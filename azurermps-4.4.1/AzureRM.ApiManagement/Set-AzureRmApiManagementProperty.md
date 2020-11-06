---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 5C0C437D-7237-4B40-A254-1B55916F1C71
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementProperty.md
ms.openlocfilehash: 5273161b18f49e2cfd8f772987d8f0d9ce90bc69
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557976"
---
# <span data-ttu-id="961b5-101">Set-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="961b5-101">Set-AzureRmApiManagementProperty</span></span>

## <span data-ttu-id="961b5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="961b5-102">SYNOPSIS</span></span>
<span data-ttu-id="961b5-103">Изменяет свойство управления API.</span><span class="sxs-lookup"><span data-stu-id="961b5-103">Modifies an API Management Property.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="961b5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="961b5-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementProperty -Context <PsApiManagementContext> -PropertyId <String> [-Name <String>]
 [-Value <String>] [-Secret <Boolean>] [-Tags <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="961b5-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="961b5-105">DESCRIPTION</span></span>
<span data-ttu-id="961b5-106">Командлет **Set-AzureRmApiManagementProperty** изменяет свойство управления API Azure.</span><span class="sxs-lookup"><span data-stu-id="961b5-106">The **Set-AzureRmApiManagementProperty** cmdlet modifies an Azure API Management Property.</span></span>

## <span data-ttu-id="961b5-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="961b5-107">EXAMPLES</span></span>

### <span data-ttu-id="961b5-108">Пример 1: изменение тегов в свойстве</span><span class="sxs-lookup"><span data-stu-id="961b5-108">Example 1: Change the tags on a property</span></span>
```
PS C:\>$Tags = 'sdk', 'powershell'
PS C:\> Set-AzureRmApiManagementProperty -Context $ApimContext -PropertyId "Property11" -Tags $Tags -PassThru
```

<span data-ttu-id="961b5-109">Первая команда присваивает переменной $Tags два значения.</span><span class="sxs-lookup"><span data-stu-id="961b5-109">The first command assigns two values to the $Tags variable.</span></span>

<span data-ttu-id="961b5-110">Вторая команда изменяет свойство с ИДЕНТИФИКАТОРом Property11.</span><span class="sxs-lookup"><span data-stu-id="961b5-110">The second command modifies the property that has the ID Property11.</span></span>
<span data-ttu-id="961b5-111">Команда назначает строки в $Tags в качестве тегов в свойстве.</span><span class="sxs-lookup"><span data-stu-id="961b5-111">The command assigns the strings in $Tags as tags on the property.</span></span>

### <span data-ttu-id="961b5-112">Пример 2: изменение свойства для его секретного значения</span><span class="sxs-lookup"><span data-stu-id="961b5-112">Example 2: Modify a property to have a secret value</span></span>
```
PS C:\>Set-AzureRmApiManagementProperty -Context $ApimContext -PropertyId "Property12" -Secret $True -PassThru
```

<span data-ttu-id="961b5-113">Эта команда изменяет свойство на зашифрование.</span><span class="sxs-lookup"><span data-stu-id="961b5-113">This command changes the property to be Encrypted.</span></span>

## <span data-ttu-id="961b5-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="961b5-114">PARAMETERS</span></span>

### <span data-ttu-id="961b5-115">-Context</span><span class="sxs-lookup"><span data-stu-id="961b5-115">-Context</span></span>
<span data-ttu-id="961b5-116">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="961b5-116">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="961b5-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="961b5-117">-Name</span></span>
<span data-ttu-id="961b5-118">Указывает имя свойства.</span><span class="sxs-lookup"><span data-stu-id="961b5-118">Specifies the name of the property.</span></span>
<span data-ttu-id="961b5-119">Максимальная длина — 100 символов.</span><span class="sxs-lookup"><span data-stu-id="961b5-119">Maximum length is 100 characters.</span></span>
<span data-ttu-id="961b5-120">Имена содержат только буквы, цифры, точки, тире и знаки подчеркивания.</span><span class="sxs-lookup"><span data-stu-id="961b5-120">Names contain only letters, digits, period, dash, and underscore characters.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="961b5-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="961b5-121">-PassThru</span></span>
<span data-ttu-id="961b5-122">Указывает на то, что этот командлет возвращает **PsApiManagementProperty** , который изменяется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="961b5-122">Indicates that this cmdlet returns the **PsApiManagementProperty** that this cmdlet modifies.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="961b5-123">-PropertyId</span><span class="sxs-lookup"><span data-stu-id="961b5-123">-PropertyId</span></span>
<span data-ttu-id="961b5-124">Указывает идентификатор свойства, которое изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="961b5-124">Specifies an ID of the property that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="961b5-125">-Secret (секретный)</span><span class="sxs-lookup"><span data-stu-id="961b5-125">-Secret</span></span>
<span data-ttu-id="961b5-126">Указывает на то, что значение свойства является секретным и должно быть зашифровано.</span><span class="sxs-lookup"><span data-stu-id="961b5-126">Indicates that the property value is a secret and should be encrypted.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="961b5-127">-Теги</span><span class="sxs-lookup"><span data-stu-id="961b5-127">-Tags</span></span>
<span data-ttu-id="961b5-128">Задает массив тегов, которым этот командлет связывается со свойством.</span><span class="sxs-lookup"><span data-stu-id="961b5-128">Specifies an array of tags that this cmdlet associates to the property.</span></span>
<span data-ttu-id="961b5-129">С помощью тегов можно отфильтровать список свойств.</span><span class="sxs-lookup"><span data-stu-id="961b5-129">You can use tags to filter the property list.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="961b5-130">-Value (значение)</span><span class="sxs-lookup"><span data-stu-id="961b5-130">-Value</span></span>
<span data-ttu-id="961b5-131">Задает значение для свойства.</span><span class="sxs-lookup"><span data-stu-id="961b5-131">Specifies a value for the property.</span></span>
<span data-ttu-id="961b5-132">Это значение может содержать выражения политики.</span><span class="sxs-lookup"><span data-stu-id="961b5-132">This value can contain policy expressions.</span></span>
<span data-ttu-id="961b5-133">Максимальная длина — 1000 символов.</span><span class="sxs-lookup"><span data-stu-id="961b5-133">Maximum length is 1000 characters.</span></span>
<span data-ttu-id="961b5-134">Значение не может быть пустым или состоять только из пробелов.</span><span class="sxs-lookup"><span data-stu-id="961b5-134">The value may not be empty or consist only of whitespace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="961b5-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="961b5-135">-DefaultProfile</span></span>
<span data-ttu-id="961b5-136">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="961b5-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="961b5-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="961b5-137">CommonParameters</span></span>
<span data-ttu-id="961b5-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="961b5-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="961b5-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="961b5-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="961b5-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="961b5-140">INPUTS</span></span>

## <span data-ttu-id="961b5-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="961b5-141">OUTPUTS</span></span>

### <span data-ttu-id="961b5-142">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="961b5-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProperty</span></span>

## <span data-ttu-id="961b5-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="961b5-143">NOTES</span></span>

## <span data-ttu-id="961b5-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="961b5-144">RELATED LINKS</span></span>

[<span data-ttu-id="961b5-145">Get-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="961b5-145">Get-AzureRmApiManagementProperty</span></span>](./Get-AzureRmApiManagementProperty.md)

[<span data-ttu-id="961b5-146">New-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="961b5-146">New-AzureRmApiManagementProperty</span></span>](./New-AzureRmApiManagementProperty.md)

[<span data-ttu-id="961b5-147">Remove-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="961b5-147">Remove-AzureRmApiManagementProperty</span></span>](./Remove-AzureRmApiManagementProperty.md)


