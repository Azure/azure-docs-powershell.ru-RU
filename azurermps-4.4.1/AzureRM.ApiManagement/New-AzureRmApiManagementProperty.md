---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: A91F93D3-B8C7-4328-A049-AB9877C1166C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementProperty.md
ms.openlocfilehash: cb50ea5735a9f63f5f35b8f1cb0648c566e6108d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734285"
---
# <span data-ttu-id="8183f-101">New-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="8183f-101">New-AzureRmApiManagementProperty</span></span>

## <span data-ttu-id="8183f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8183f-102">SYNOPSIS</span></span>
<span data-ttu-id="8183f-103">Создает новое свойство.</span><span class="sxs-lookup"><span data-stu-id="8183f-103">Creates a new Property.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8183f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8183f-104">SYNTAX</span></span>

```
New-AzureRmApiManagementProperty -Context <PsApiManagementContext> [-PropertyId <String>] -Name <String>
 -Value <String> [-Secret] [-Tags <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8183f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8183f-105">DESCRIPTION</span></span>
<span data-ttu-id="8183f-106">Командлет **New-AzureRmApiManagementProperty** создает **свойство** управления API Azure.</span><span class="sxs-lookup"><span data-stu-id="8183f-106">The **New-AzureRmApiManagementProperty** cmdlet creates an Azure API Management **Property**.</span></span>

## <span data-ttu-id="8183f-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8183f-107">EXAMPLES</span></span>

### <span data-ttu-id="8183f-108">Пример 1: Создание свойства, включающего Теги</span><span class="sxs-lookup"><span data-stu-id="8183f-108">Example 1: Create a property that includes tags</span></span>
```
PS C:\>$Tags = 'sdk', 'powershell'
PS C:\> New-AzureRmApiManagementProperty -Context $ApimContext -PropertyId "Property11" -Name "Property Name" -Value "Property Value" -Tags $Tags
```

<span data-ttu-id="8183f-109">Первая команда присваивает переменной $Tags два значения.</span><span class="sxs-lookup"><span data-stu-id="8183f-109">The first command assigns two values to the $Tags variable.</span></span>

<span data-ttu-id="8183f-110">Вторая команда создает свойство и присваивает строки в $Tags как теги в свойстве.</span><span class="sxs-lookup"><span data-stu-id="8183f-110">The second command creates a property and assigns the strings in $Tags as tags on the property.</span></span>

### <span data-ttu-id="8183f-111">Пример 2: Создание свойства с секретным значением</span><span class="sxs-lookup"><span data-stu-id="8183f-111">Example 2: Create a property that has a secret value</span></span>
```
PS C:\>New-AzureRmApiManagementProperty -Context $apimContext -PropertyId "Property12" -Name "Secret Property -Value "Secret Property Value" -Secret
```

<span data-ttu-id="8183f-112">Эта команда создает **свойство** с зашифрованным значением.</span><span class="sxs-lookup"><span data-stu-id="8183f-112">This command creates a **Property** that has a value that is encrypted.</span></span>

## <span data-ttu-id="8183f-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8183f-113">PARAMETERS</span></span>

### <span data-ttu-id="8183f-114">-Context</span><span class="sxs-lookup"><span data-stu-id="8183f-114">-Context</span></span>
<span data-ttu-id="8183f-115">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="8183f-115">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="8183f-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8183f-116">-Name</span></span>
<span data-ttu-id="8183f-117">Указывает имя свойства, создаваемого этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="8183f-117">Specifies the name of the property that this cmdlet creates.</span></span>
<span data-ttu-id="8183f-118">Максимальная длина — 100 символов.</span><span class="sxs-lookup"><span data-stu-id="8183f-118">Maximum length is 100 characters.</span></span>
<span data-ttu-id="8183f-119">Имена содержат только буквы, цифры, точки, тире и знаки подчеркивания.</span><span class="sxs-lookup"><span data-stu-id="8183f-119">Names contain only letters, digits, period, dash, and underscore characters.</span></span>

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

### <span data-ttu-id="8183f-120">-PropertyId</span><span class="sxs-lookup"><span data-stu-id="8183f-120">-PropertyId</span></span>
<span data-ttu-id="8183f-121">Задает идентификатор для свойства.</span><span class="sxs-lookup"><span data-stu-id="8183f-121">Specifies an ID for the property.</span></span>
<span data-ttu-id="8183f-122">Максимальная длина — 256 символов.</span><span class="sxs-lookup"><span data-stu-id="8183f-122">Maximum length is 256 characters.</span></span>
<span data-ttu-id="8183f-123">Если идентификатор не указан, этот командлет создаст его.</span><span class="sxs-lookup"><span data-stu-id="8183f-123">If you do not specify an ID, this cmdlet generates one.</span></span>

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

### <span data-ttu-id="8183f-124">-Secret (секретный)</span><span class="sxs-lookup"><span data-stu-id="8183f-124">-Secret</span></span>
<span data-ttu-id="8183f-125">Указывает на то, что значение свойства является секретным и должно быть зашифровано.</span><span class="sxs-lookup"><span data-stu-id="8183f-125">Indicates that the property value is a secret and should be encrypted.</span></span>

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

### <span data-ttu-id="8183f-126">-Теги</span><span class="sxs-lookup"><span data-stu-id="8183f-126">-Tags</span></span>
<span data-ttu-id="8183f-127">Задает массив тегов, которым этот командлет связывается со свойством.</span><span class="sxs-lookup"><span data-stu-id="8183f-127">Specifies an array of tags that this cmdlet associates to the property.</span></span>
<span data-ttu-id="8183f-128">С помощью тегов можно отфильтровать список свойств.</span><span class="sxs-lookup"><span data-stu-id="8183f-128">You can use tags to filter the property list.</span></span>

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

### <span data-ttu-id="8183f-129">-Value (значение)</span><span class="sxs-lookup"><span data-stu-id="8183f-129">-Value</span></span>
<span data-ttu-id="8183f-130">Задает значение для свойства.</span><span class="sxs-lookup"><span data-stu-id="8183f-130">Specifies a value for the property.</span></span>
<span data-ttu-id="8183f-131">Это значение может содержать выражения политики.</span><span class="sxs-lookup"><span data-stu-id="8183f-131">This value can contain policy expressions.</span></span>
<span data-ttu-id="8183f-132">Максимальная длина — 1000 символов.</span><span class="sxs-lookup"><span data-stu-id="8183f-132">Maximum length is 1000 characters.</span></span>
<span data-ttu-id="8183f-133">Значение не может быть пустым или состоять только из пробелов.</span><span class="sxs-lookup"><span data-stu-id="8183f-133">The value may not be empty or consist only of whitespace.</span></span>

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

### <span data-ttu-id="8183f-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8183f-134">-DefaultProfile</span></span>
<span data-ttu-id="8183f-135">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8183f-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8183f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8183f-136">CommonParameters</span></span>
<span data-ttu-id="8183f-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8183f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8183f-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8183f-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8183f-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8183f-139">INPUTS</span></span>

## <span data-ttu-id="8183f-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8183f-140">OUTPUTS</span></span>

### <span data-ttu-id="8183f-141">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="8183f-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProperty</span></span>

## <span data-ttu-id="8183f-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="8183f-142">NOTES</span></span>

## <span data-ttu-id="8183f-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8183f-143">RELATED LINKS</span></span>

[<span data-ttu-id="8183f-144">Remove-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="8183f-144">Remove-AzureRmApiManagementProperty</span></span>](./Remove-AzureRmApiManagementProperty.md)

[<span data-ttu-id="8183f-145">Set-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="8183f-145">Set-AzureRmApiManagementProperty</span></span>](./Set-AzureRmApiManagementProperty.md)


