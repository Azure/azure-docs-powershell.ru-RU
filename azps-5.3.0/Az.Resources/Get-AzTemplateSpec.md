---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-aztemplatespec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTemplateSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTemplateSpec.md
ms.openlocfilehash: be3a16707303016e22be8052721efcb35c608b3e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98505252"
---
# <span data-ttu-id="48066-101">Get-AzTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="48066-101">Get-AzTemplateSpec</span></span>

## <span data-ttu-id="48066-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="48066-102">SYNOPSIS</span></span>
<span data-ttu-id="48066-103">Возвращает или перечисляет спецификации шаблона.</span><span class="sxs-lookup"><span data-stu-id="48066-103">Gets or lists Template Specs</span></span>

## <span data-ttu-id="48066-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="48066-104">SYNTAX</span></span>

### <span data-ttu-id="48066-105">ListTemplateSpecsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="48066-105">ListTemplateSpecsParameterSet (Default)</span></span>
```
Get-AzTemplateSpec [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="48066-106">GetTemplateSpecByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="48066-106">GetTemplateSpecByNameParameterSet</span></span>
```
Get-AzTemplateSpec [-ResourceGroupName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="48066-107">GetTemplateSpecByIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="48066-107">GetTemplateSpecByIdParameterSet</span></span>
```
Get-AzTemplateSpec [[-Version] <String>] [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="48066-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="48066-108">DESCRIPTION</span></span>
<span data-ttu-id="48066-109">С помощью этого cmdlet можно использовать для списка спецификаций шаблона в группе подписок и ресурсов или получения определенной спецификации шаблона по имени или коду. При получении определенной спецификации шаблона по имени или ид можно при желании получить конкретную версию, указав имя версии с помощью параметра **-Version.**</span><span class="sxs-lookup"><span data-stu-id="48066-109">This cmdlet can be used to list Template Specs in a subscription/resource group or get a specific Template Spec by name or id. When getting a specific Template Spec by name/id a specific version can optionally be retrieved by specifying a version name through the **-Version** parameter.</span></span> <span data-ttu-id="48066-110">Если **используется версия** -, в пределах \* будут представлены только конкретные сведения о *версии. Версии возвращенного* объекта Template Spec.</span><span class="sxs-lookup"><span data-stu-id="48066-110">When **-Version** is used, only the specific version details will be present within \**.Versions* on the returned Template Spec object.</span></span> <span data-ttu-id="48066-111">Если при искомой спецификации шаблона не указана конкретная версия, будут представлены все версии в формате \**. Свойство Версий* возвращаемого объекта.</span><span class="sxs-lookup"><span data-stu-id="48066-111">If no specific version is specified when retrieving a Template Spec by name/id, all versions will be present within the  \**.Versions* property of the returned object.</span></span>

<span data-ttu-id="48066-112">**Примечание.** При перечислении всех спецификаций шаблона в рамках подписки или группы ресурсов каждый возвращаемый шаблон *". Свойство Versions* (Версии) будет *иметь null.*</span><span class="sxs-lookup"><span data-stu-id="48066-112">**Note**: When listing all Template Specs within a subscription or resource group, each returned Template Spec's *".Versions"* property will be *null*.</span></span> <span data-ttu-id="48066-113">Сведения о версии включаются только в том случае, если заданы параметры -Name или -ResourceId (например, вы запрашиваете определенный шаблон спецификации/версии).</span><span class="sxs-lookup"><span data-stu-id="48066-113">Version information is only included when -Name or -ResourceId parameters are provided (eg: you are requesting a specific template spec/version).</span></span>

## <span data-ttu-id="48066-114">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="48066-114">EXAMPLES</span></span>

### <span data-ttu-id="48066-115">Пример 1. Спецификации шаблона списка в текущей подписке</span><span class="sxs-lookup"><span data-stu-id="48066-115">Example 1: List Template Specs in current subscription</span></span>
```powershell
PS C:\> Get-AzTemplateSpec
```

<span data-ttu-id="48066-116">Список всех спецификаций шаблона в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="48066-116">Lists all Template Specs in the current subscription.</span></span>

### <span data-ttu-id="48066-117">Пример 2. Спецификации шаблона списка в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="48066-117">Example 2: List Template Specs in a resource group</span></span>
```powershell
PS C:\> Get-AzTemplateSpec -ResourceGroupName 'myRG'
```

<span data-ttu-id="48066-118">Список всех спецификаций шаблона в группе ресурсов MyRG текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="48066-118">Lists all Template Specs in the resource group 'myRG' of the current subscription.</span></span>

### <span data-ttu-id="48066-119">Пример 3. Получить спецификацию шаблона (со всеми версиями) по имени</span><span class="sxs-lookup"><span data-stu-id="48066-119">Example 3: Get Template Spec (with all versions) by name</span></span>
```powershell
PS C:\> Get-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec'
```

<span data-ttu-id="48066-120">Возвращает сведения о спецификации шаблона MyTemplateSpec в группе ресурсов myRG.</span><span class="sxs-lookup"><span data-stu-id="48066-120">Gets information about the Template Spec named 'MyTemplateSpec' within the resource group 'myRG'.</span></span>

<span data-ttu-id="48066-121">**Примечание.** Все версии шаблона Спецификации будут представлены в *Свойство Versions*(Версии) возвращаемого объекта.</span><span class="sxs-lookup"><span data-stu-id="48066-121">**Note**: All of the Template Spec's versions will be present within the "*.Versions*" property of the return object.</span></span>

### <span data-ttu-id="48066-122">Пример 4. Получить шаблон спецификации (конкретную версию) по имени</span><span class="sxs-lookup"><span data-stu-id="48066-122">Example 4: Get Template Spec (specific version) by name</span></span>
```powershell
PS C:\> Get-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec' -Version 'v1.0'
```

<span data-ttu-id="48066-123">Сведения о версии "v1.0" спецификации шаблона "MyTemplateSpec" в группе ресурсов myRG.</span><span class="sxs-lookup"><span data-stu-id="48066-123">Gets information about version 'v1.0' of the Template Spec named 'MyTemplateSpec' within the resource group 'myRG'.</span></span>

<span data-ttu-id="48066-124">**Примечание.** *Свойство «Версии»* возвращаемого объекта будет содержать только запросятую версию.</span><span class="sxs-lookup"><span data-stu-id="48066-124">**Note**: The *".Versions"* property of the returned object will contain only the specific version requested.</span></span>

### <span data-ttu-id="48066-125">Пример 5. Получить спецификацию шаблона (со всеми версиями) по ид ресурса</span><span class="sxs-lookup"><span data-stu-id="48066-125">Example 5: Get Template Spec (with all versions) by resource id</span></span>
```powershell
PS C:\> Get-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec'
```

<span data-ttu-id="48066-126">Возвращает сведения о спецификации шаблона с именем "MyTemplateSpec" в группе ресурсов myRG подид \{ \} подписки.</span><span class="sxs-lookup"><span data-stu-id="48066-126">Gets information about the Template Spec named 'MyTemplateSpec' within the resource group 'myRG' of subscription \{subId\}.</span></span>

<span data-ttu-id="48066-127">**Примечание.** Все версии шаблона Спецификации будут представлены в *Свойство Versions*(Версии) возвращаемого объекта.</span><span class="sxs-lookup"><span data-stu-id="48066-127">**Note**: All of the Template Spec's versions will be present within the "*.Versions*" property of the return object.</span></span>

### <span data-ttu-id="48066-128">Пример 6. Получить спецификацию шаблона (конкретную версию) по ид ресурса</span><span class="sxs-lookup"><span data-stu-id="48066-128">Example 6: Get Template Spec (specific version) by resource id</span></span>
```powershell
PS C:\> Get-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec' -Version 'v1.0'
```

<span data-ttu-id="48066-129">Получает сведения о версии "v1.0" спецификации шаблона "MyTemplateSpec" в группе ресурсов myRG из \{ subId \} подписки.</span><span class="sxs-lookup"><span data-stu-id="48066-129">Gets information about version 'v1.0' of the Template Spec named 'MyTemplateSpec' within the resource group 'myRG' of subscription \{subId\}.</span></span>

<span data-ttu-id="48066-130">**Примечание.** *Свойство «Версии»* возвращаемого объекта будет содержать только запросятую версию.</span><span class="sxs-lookup"><span data-stu-id="48066-130">**Note**: The *".Versions"* property of the returned object will contain only the specific version requested.</span></span>

## <span data-ttu-id="48066-131">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="48066-131">PARAMETERS</span></span>

### <span data-ttu-id="48066-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48066-132">-DefaultProfile</span></span>
<span data-ttu-id="48066-133">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="48066-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="48066-134">-Name</span><span class="sxs-lookup"><span data-stu-id="48066-134">-Name</span></span>
<span data-ttu-id="48066-135">Имя спецификации шаблона.</span><span class="sxs-lookup"><span data-stu-id="48066-135">The name of the template spec.</span></span>

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

### <span data-ttu-id="48066-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48066-136">-ResourceGroupName</span></span>
<span data-ttu-id="48066-137">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="48066-137">The name of the resource group.</span></span>

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

### <span data-ttu-id="48066-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="48066-138">-ResourceId</span></span>
<span data-ttu-id="48066-139">Полное имя ресурса спецификации шаблона. Пример: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span><span class="sxs-lookup"><span data-stu-id="48066-139">The fully qualified resource Id of the template spec. Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span></span>

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

### <span data-ttu-id="48066-140">-Версия</span><span class="sxs-lookup"><span data-stu-id="48066-140">-Version</span></span>
<span data-ttu-id="48066-141">Версия спецификации шаблона.</span><span class="sxs-lookup"><span data-stu-id="48066-141">The version of the template spec.</span></span>

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

### <span data-ttu-id="48066-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48066-142">CommonParameters</span></span>
<span data-ttu-id="48066-143">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48066-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48066-144">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="48066-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48066-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="48066-145">INPUTS</span></span>

### <span data-ttu-id="48066-146">System.String</span><span class="sxs-lookup"><span data-stu-id="48066-146">System.String</span></span>

## <span data-ttu-id="48066-147">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="48066-147">OUTPUTS</span></span>

### <span data-ttu-id="48066-148">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="48066-148">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplateSpec</span></span>

## <span data-ttu-id="48066-149">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="48066-149">NOTES</span></span>

## <span data-ttu-id="48066-150">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="48066-150">RELATED LINKS</span></span>
