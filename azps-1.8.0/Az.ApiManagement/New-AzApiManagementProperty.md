---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: A91F93D3-B8C7-4328-A049-AB9877C1166C
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementProperty.md
ms.openlocfilehash: d54665b767d10edde564450ecfcdd467b784dd8b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93901729"
---
# <span data-ttu-id="0da49-101">New-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="0da49-101">New-AzApiManagementProperty</span></span>

## <span data-ttu-id="0da49-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0da49-102">SYNOPSIS</span></span>
<span data-ttu-id="0da49-103">Создает новое свойство.</span><span class="sxs-lookup"><span data-stu-id="0da49-103">Creates a new Property.</span></span>

## <span data-ttu-id="0da49-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0da49-104">SYNTAX</span></span>

```
New-AzApiManagementProperty -Context <PsApiManagementContext> [-PropertyId <String>] -Name <String>
 -Value <String> [-Secret] [-Tag <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0da49-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0da49-105">DESCRIPTION</span></span>
<span data-ttu-id="0da49-106">Командлет **New-AzApiManagementProperty** создает **свойство** управления API Azure.</span><span class="sxs-lookup"><span data-stu-id="0da49-106">The **New-AzApiManagementProperty** cmdlet creates an Azure API Management **Property**.</span></span>

## <span data-ttu-id="0da49-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0da49-107">EXAMPLES</span></span>

### <span data-ttu-id="0da49-108">Пример 1: Создание свойства, включающего Теги</span><span class="sxs-lookup"><span data-stu-id="0da49-108">Example 1: Create a property that includes tags</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$Tags = 'sdk', 'powershell'
PS C:\> New-AzApiManagementProperty -Context $apimContext -PropertyId "Property11" -Name "Property Name" -Value "Property Value" -Tags $Tags
```

<span data-ttu-id="0da49-109">Первая команда присваивает переменной $Tags два значения.</span><span class="sxs-lookup"><span data-stu-id="0da49-109">The first command assigns two values to the $Tags variable.</span></span>
<span data-ttu-id="0da49-110">Вторая команда создает свойство и присваивает строки в $Tags как теги в свойстве.</span><span class="sxs-lookup"><span data-stu-id="0da49-110">The second command creates a property and assigns the strings in $Tags as tags on the property.</span></span>

### <span data-ttu-id="0da49-111">Пример 2: Создание свойства с секретным значением</span><span class="sxs-lookup"><span data-stu-id="0da49-111">Example 2: Create a property that has a secret value</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementProperty -Context $apimContext -PropertyId "Property12" -Name "Secret Property -Value "Secret Property Value" -Secret
```

<span data-ttu-id="0da49-112">Эта команда создает **свойство** с зашифрованным значением.</span><span class="sxs-lookup"><span data-stu-id="0da49-112">This command creates a **Property** that has a value that is encrypted.</span></span>

## <span data-ttu-id="0da49-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0da49-113">PARAMETERS</span></span>

### <span data-ttu-id="0da49-114">-Context</span><span class="sxs-lookup"><span data-stu-id="0da49-114">-Context</span></span>
<span data-ttu-id="0da49-115">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="0da49-115">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="0da49-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0da49-116">-DefaultProfile</span></span>
<span data-ttu-id="0da49-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0da49-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0da49-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0da49-118">-Name</span></span>
<span data-ttu-id="0da49-119">Указывает имя свойства, создаваемого этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="0da49-119">Specifies the name of the property that this cmdlet creates.</span></span>
<span data-ttu-id="0da49-120">Максимальная длина — 100 символов.</span><span class="sxs-lookup"><span data-stu-id="0da49-120">Maximum length is 100 characters.</span></span>
<span data-ttu-id="0da49-121">Имена содержат только буквы, цифры, точки, тире и знаки подчеркивания.</span><span class="sxs-lookup"><span data-stu-id="0da49-121">Names contain only letters, digits, period, dash, and underscore characters.</span></span>

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

### <span data-ttu-id="0da49-122">-PropertyId</span><span class="sxs-lookup"><span data-stu-id="0da49-122">-PropertyId</span></span>
<span data-ttu-id="0da49-123">Задает идентификатор для свойства.</span><span class="sxs-lookup"><span data-stu-id="0da49-123">Specifies an ID for the property.</span></span>
<span data-ttu-id="0da49-124">Максимальная длина — 256 символов.</span><span class="sxs-lookup"><span data-stu-id="0da49-124">Maximum length is 256 characters.</span></span>
<span data-ttu-id="0da49-125">Если идентификатор не указан, этот командлет создаст его.</span><span class="sxs-lookup"><span data-stu-id="0da49-125">If you do not specify an ID, this cmdlet generates one.</span></span>

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

### <span data-ttu-id="0da49-126">-Secret (секретный)</span><span class="sxs-lookup"><span data-stu-id="0da49-126">-Secret</span></span>
<span data-ttu-id="0da49-127">Указывает на то, что значение свойства является секретным и должно быть зашифровано.</span><span class="sxs-lookup"><span data-stu-id="0da49-127">Indicates that the property value is a secret and should be encrypted.</span></span>

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

### <span data-ttu-id="0da49-128">-Тег</span><span class="sxs-lookup"><span data-stu-id="0da49-128">-Tag</span></span>
<span data-ttu-id="0da49-129">Теги, связанные с свойством.</span><span class="sxs-lookup"><span data-stu-id="0da49-129">Tags to be associated with Property.</span></span> <span data-ttu-id="0da49-130">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="0da49-130">This parameter is optional.</span></span>

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

### <span data-ttu-id="0da49-131">-Value (значение)</span><span class="sxs-lookup"><span data-stu-id="0da49-131">-Value</span></span>
<span data-ttu-id="0da49-132">Задает значение для свойства.</span><span class="sxs-lookup"><span data-stu-id="0da49-132">Specifies a value for the property.</span></span>
<span data-ttu-id="0da49-133">Это значение может содержать выражения политики.</span><span class="sxs-lookup"><span data-stu-id="0da49-133">This value can contain policy expressions.</span></span>
<span data-ttu-id="0da49-134">Максимальная длина — 1000 символов.</span><span class="sxs-lookup"><span data-stu-id="0da49-134">Maximum length is 1000 characters.</span></span>
<span data-ttu-id="0da49-135">Значение не может быть пустым или состоять только из пробелов.</span><span class="sxs-lookup"><span data-stu-id="0da49-135">The value may not be empty or consist only of whitespace.</span></span>

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

### <span data-ttu-id="0da49-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0da49-136">CommonParameters</span></span>
<span data-ttu-id="0da49-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0da49-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0da49-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0da49-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0da49-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0da49-139">INPUTS</span></span>

### <span data-ttu-id="0da49-140">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="0da49-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="0da49-141">System. String</span><span class="sxs-lookup"><span data-stu-id="0da49-141">System.String</span></span>

### <span data-ttu-id="0da49-142">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="0da49-142">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="0da49-143">System. String []</span><span class="sxs-lookup"><span data-stu-id="0da49-143">System.String[]</span></span>

## <span data-ttu-id="0da49-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0da49-144">OUTPUTS</span></span>

### <span data-ttu-id="0da49-145">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="0da49-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProperty</span></span>

## <span data-ttu-id="0da49-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="0da49-146">NOTES</span></span>

## <span data-ttu-id="0da49-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0da49-147">RELATED LINKS</span></span>

[<span data-ttu-id="0da49-148">Remove-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="0da49-148">Remove-AzApiManagementProperty</span></span>](./Remove-AzApiManagementProperty.md)

[<span data-ttu-id="0da49-149">Set-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="0da49-149">Set-AzApiManagementProperty</span></span>](./Set-AzApiManagementProperty.md)


