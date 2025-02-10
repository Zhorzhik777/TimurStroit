import { Card, CardContent } from "@/components/ui/card";
import { Button } from "@/components/ui/button";
import { Tabs, TabsList, TabsTrigger, TabsContent } from "@/components/ui/tabs";
import { Image, FileText, CheckCircle, DollarSign, Video } from "lucide-react";

export default function App() {
  return (
    <div className="p-4 max-w-md mx-auto">
      <h1 className="text-xl font-bold text-center mb-4">Объект строительства</h1>
      
      <Tabs defaultValue="photos" className="w-full">
        <TabsList className="grid grid-cols-5 mb-4">
          <TabsTrigger value="photos"><Image className="mr-2" />Фото</TabsTrigger>
          <TabsTrigger value="documents"><FileText className="mr-2" />Документы</TabsTrigger>
          <TabsTrigger value="acts"><CheckCircle className="mr-2" />Акты</TabsTrigger>
          <TabsTrigger value="estimates"><DollarSign className="mr-2" />Сметы</TabsTrigger>
          <TabsTrigger value="stream"><Video className="mr-2" />Трансляция</TabsTrigger>
        </TabsList>
        
        <TabsContent value="photos">
          <Card><CardContent>📸 Галерея хода работ</CardContent></Card>
        </TabsContent>
        
        <TabsContent value="documents">
          <Card><CardContent>📂 Документы объекта</CardContent></Card>
        </TabsContent>
        
        <TabsContent value="acts">
          <Card><CardContent>✅ Подписание актов</CardContent></Card>
        </TabsContent>

        <TabsContent value="estimates">
          <Card><CardContent>💰 Отображение смет</CardContent></Card>
        </TabsContent>

        <TabsContent value="stream">
          <Card><CardContent>🎥 Прямая трансляция с объекта</CardContent></Card>
        </TabsContent>
      </Tabs>
      
      <Button className="w-full mt-4">Добавить фото / документ</Button>
    </div>
  );
}
