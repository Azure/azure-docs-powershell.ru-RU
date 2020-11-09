---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-aztemplatespec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTemplateSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTemplateSpec.md
ms.openlocfilehash: be3a16707303016e22be8052721efcb35c608b3e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94316391"
---
# <span data-ttu-id="351f8-101">Get-AzTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="351f8-101">Get-AzTemplateSpec</span></span>

## <span data-ttu-id="351f8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="351f8-102">SYNOPSIS</span></span>
<span data-ttu-id="351f8-103">Возвращает или приводит список спецификаций шаблонов</span><span class="sxs-lookup"><span data-stu-id="351f8-103">Gets or lists Template Specs</span></span>

## <span data-ttu-id="351f8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="351f8-104">SYNTAX</span></span>

### <span data-ttu-id="351f8-105">ListTemplateSpecsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="351f8-105">ListTemplateSpecsParameterSet (Default)</span></span>
```
Get-AzTemplateSpec [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="351f8-106">GetTemplateSpecByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="351f8-106">GetTemplateSpecByNameParameterSet</span></span>
```
Get-AzTemplateSpec [-ResourceGroupName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="351f8-107">GetTemplateSpecByIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="351f8-107">GetTemplateSpecByIdParameterSet</span></span>
```
Get-AzTemplateSpec [[-Version] <String>] [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="351f8-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="351f8-108">DESCRIPTION</span></span>
<span data-ttu-id="351f8-109">Этот командлет можно использовать для получения спецификаций шаблонов в подписке или группе ресурсов, а также при получении определенных спецификаций шаблонов по имени или идентификатору. При получении определенных спецификаций шаблона по имени или идентификатору можно дополнительно извлечь определенную версию, указав ее имя с помощью параметра **-Version** .</span><span class="sxs-lookup"><span data-stu-id="351f8-109">This cmdlet can be used to list Template Specs in a subscription/resource group or get a specific Template Spec by name or id. When getting a specific Template Spec by name/id a specific version can optionally be retrieved by specifying a version name through the **-Version** parameter.</span></span> <span data-ttu-id="351f8-110">Когда используется **Версия-Version** , в течение \* может быть указана только определенная информация о версии *. Версии* возвращаемого объекта Spec шаблона.</span><span class="sxs-lookup"><span data-stu-id="351f8-110">When **-Version** is used, only the specific version details will be present within \* *.Versions* on the returned Template Spec object.</span></span> <span data-ttu-id="351f8-111">Если при извлечении спецификаций шаблона по имени или идентификатору не указана какая-либо определенная версия, все версии будут указаны в разделе \* *. Свойство Versions* возвращаемого объекта.</span><span class="sxs-lookup"><span data-stu-id="351f8-111">If no specific version is specified when retrieving a Template Spec by name/id, all versions will be present within the  \* *.Versions* property of the returned object.</span></span>

<span data-ttu-id="351f8-112">**Примечание**. при составлении списка всех спецификаций шаблонов в подписке или группе ресурсов каждый возвращенный шаблон спецификации *". Versions* будет *значение NULL*.</span><span class="sxs-lookup"><span data-stu-id="351f8-112">**Note** : When listing all Template Specs within a subscription or resource group, each returned Template Spec's *".Versions"* property will be *null*.</span></span> <span data-ttu-id="351f8-113">Сведения о версии включаются только в том случае, если указаны параметры-Name или-ResourceId (например, вы запрашиваете определенную спецификацию и версию шаблона).</span><span class="sxs-lookup"><span data-stu-id="351f8-113">Version information is only included when -Name or -ResourceId parameters are provided (eg: you are requesting a specific template spec/version).</span></span>

## <span data-ttu-id="351f8-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="351f8-114">EXAMPLES</span></span>

### <span data-ttu-id="351f8-115">Пример 1: спецификации шаблона списка в текущей подписке</span><span class="sxs-lookup"><span data-stu-id="351f8-115">Example 1: List Template Specs in current subscription</span></span>
```powershell
PS C:\> Get-AzTemplateSpec
```

<span data-ttu-id="351f8-116">Список всех спецификаций шаблонов в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="351f8-116">Lists all Template Specs in the current subscription.</span></span>

### <span data-ttu-id="351f8-117">Пример 2: спецификации шаблона списка в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="351f8-117">Example 2: List Template Specs in a resource group</span></span>
```powershell
PS C:\> Get-AzTemplateSpec -ResourceGroupName 'myRG'
```

<span data-ttu-id="351f8-118">Список всех спецификаций шаблонов в группе ресурсов "myRG" текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="351f8-118">Lists all Template Specs in the resource group 'myRG' of the current subscription.</span></span>

### <span data-ttu-id="351f8-119">Пример 3: получение спецификации шаблона (со всеми версиями) по названию</span><span class="sxs-lookup"><span data-stu-id="351f8-119">Example 3: Get Template Spec (with all versions) by name</span></span>
```powershell
PS C:\> Get-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec'
```

<span data-ttu-id="351f8-120">Возвращает сведения о спецификации Template с именем "MyTemplateSpec" в группе ресурсов "myRG".</span><span class="sxs-lookup"><span data-stu-id="351f8-120">Gets information about the Template Spec named 'MyTemplateSpec' within the resource group 'myRG'.</span></span>

<span data-ttu-id="351f8-121">**Примечание**. все версии спецификации шаблона будут представлены в разделе " *. Свойство "Versions* " возвращаемого объекта.</span><span class="sxs-lookup"><span data-stu-id="351f8-121">**Note** : All of the Template Spec's versions will be present within the " *.Versions* " property of the return object.</span></span>

### <span data-ttu-id="351f8-122">Пример 4: получение спецификации шаблона (конкретной версии) по названию</span><span class="sxs-lookup"><span data-stu-id="351f8-122">Example 4: Get Template Spec (specific version) by name</span></span>
```powershell
PS C:\> Get-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec' -Version 'v1.0'
```

<span data-ttu-id="351f8-123">Возвращает сведения о версии "v 1.0" спецификации шаблона с именем "MyTemplateSpec" в группе ресурсов "myRG".</span><span class="sxs-lookup"><span data-stu-id="351f8-123">Gets information about version 'v1.0' of the Template Spec named 'MyTemplateSpec' within the resource group 'myRG'.</span></span>

<span data-ttu-id="351f8-124">**Примечание** : *". Свойство Versions* возвращаемого объекта будет содержать только определенную версию.</span><span class="sxs-lookup"><span data-stu-id="351f8-124">**Note** : The *".Versions"* property of the returned object will contain only the specific version requested.</span></span>

### <span data-ttu-id="351f8-125">Пример 5: получение спецификаций шаблона (со всеми версиями) по идентификатору ресурса</span><span class="sxs-lookup"><span data-stu-id="351f8-125">Example 5: Get Template Spec (with all versions) by resource id</span></span>
```powershell
PS C:\> Get-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec'
```

<span data-ttu-id="351f8-126">Возвращает сведения о спецификации Template с именем "MyTemplateSpec" в группе ресурсов "myRG" в \{ subId подписку \} .</span><span class="sxs-lookup"><span data-stu-id="351f8-126">Gets information about the Template Spec named 'MyTemplateSpec' within the resource group 'myRG' of subscription \{subId\}.</span></span>

<span data-ttu-id="351f8-127">**Примечание**. все версии спецификации шаблона будут представлены в разделе " *. Свойство "Versions* " возвращаемого объекта.</span><span class="sxs-lookup"><span data-stu-id="351f8-127">**Note** : All of the Template Spec's versions will be present within the " *.Versions* " property of the return object.</span></span>

### <span data-ttu-id="351f8-128">Пример 6: получение спецификации шаблона (конкретной версии) по идентификатору ресурса</span><span class="sxs-lookup"><span data-stu-id="351f8-128">Example 6: Get Template Spec (specific version) by resource id</span></span>
```powershell
PS C:\> Get-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec' -Version 'v1.0'
```

<span data-ttu-id="351f8-129">Возвращает сведения о версии "v 1.0" спецификации шаблона с именем "MyTemplateSpec" в группе ресурсов "myRG" для подписки \{ subId \} .</span><span class="sxs-lookup"><span data-stu-id="351f8-129">Gets information about version 'v1.0' of the Template Spec named 'MyTemplateSpec' within the resource group 'myRG' of subscription \{subId\}.</span></span>

<span data-ttu-id="351f8-130">**Примечание** : *". Свойство Versions* возвращаемого объекта будет содержать только определенную версию.</span><span class="sxs-lookup"><span data-stu-id="351f8-130">**Note** : The *".Versions"* property of the returned object will contain only the specific version requested.</span></span>

## <span data-ttu-id="351f8-131">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="351f8-131">PARAMETERS</span></span>

### <span data-ttu-id="351f8-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="351f8-132">-DefaultProfile</span></span>
<span data-ttu-id="351f8-133">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="351f8-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="351f8-134">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="351f8-134">-Name</span></span>
<span data-ttu-id="351f8-135">Название спецификации шаблона.</span><span class="sxs-lookup"><span data-stu-id="351f8-135">The name of the template spec.</span></span>

```yaml
Type: System.String
Parameter Sets: GetTemplateSpecByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="351f8-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="351f8-136">-ResourceGroupName</span></span>
<span data-ttu-id="351f8-137">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="351f8-137">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ListTemplateSpecsParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetTemplateSpecByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="351f8-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="351f8-138">-ResourceId</span></span>
<span data-ttu-id="351f8-139">Полный идентификатор ресурса спецификации шаблона. Пример:/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span><span class="sxs-lookup"><span data-stu-id="351f8-139">The fully qualified resource Id of the template spec. Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span></span>

```yaml
Type: System.String
Parameter Sets: GetTemplateSpecByIdParameterSet
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="351f8-140">-Version</span><span class="sxs-lookup"><span data-stu-id="351f8-140">-Version</span></span>
<span data-ttu-id="351f8-141">Версия спецификации шаблона.</span><span class="sxs-lookup"><span data-stu-id="351f8-141">The version of the template spec.</span></span>

```yaml
Type: System.String
Parameter Sets: GetTemplateSpecByNameParameterSet, GetTemplateSpecByIdParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="351f8-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="351f8-142">CommonParameters</span></span>
<span data-ttu-id="351f8-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="351f8-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="351f8-144">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="351f8-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="351f8-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="351f8-145">INPUTS</span></span>

### <span data-ttu-id="351f8-146">System. String</span><span class="sxs-lookup"><span data-stu-id="351f8-146">System.String</span></span>

## <span data-ttu-id="351f8-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="351f8-147">OUTPUTS</span></span>

### <span data-ttu-id="351f8-148">Microsoft. Azure. Commands. ResourceManager. командлеты. SdkModels. PSTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="351f8-148">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplateSpec</span></span>

## <span data-ttu-id="351f8-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="351f8-149">NOTES</span></span>

## <span data-ttu-id="351f8-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="351f8-150">RELATED LINKS</span></span>
