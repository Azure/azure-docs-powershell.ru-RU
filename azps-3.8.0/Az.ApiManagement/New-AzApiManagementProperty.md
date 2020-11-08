---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: A91F93D3-B8C7-4328-A049-AB9877C1166C
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementProperty.md
ms.openlocfilehash: bed6126dbd1ea57a29d041daf10a3deb05f2dc92
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066691"
---
# <span data-ttu-id="4c3a6-101">New-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="4c3a6-101">New-AzApiManagementProperty</span></span>

## <span data-ttu-id="4c3a6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4c3a6-102">SYNOPSIS</span></span>
<span data-ttu-id="4c3a6-103">Создает новое свойство.</span><span class="sxs-lookup"><span data-stu-id="4c3a6-103">Creates a new Property.</span></span>

## <span data-ttu-id="4c3a6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4c3a6-104">SYNTAX</span></span>

```
New-AzApiManagementProperty -Context <PsApiManagementContext> [-PropertyId <String>] -Name <String>
 -Value <String> [-Secret] [-Tag <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4c3a6-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4c3a6-105">DESCRIPTION</span></span>
<span data-ttu-id="4c3a6-106">Командлет **New-AzApiManagementProperty** создает **свойство** управления API Azure.</span><span class="sxs-lookup"><span data-stu-id="4c3a6-106">The **New-AzApiManagementProperty** cmdlet creates an Azure API Management **Property**.</span></span>

## <span data-ttu-id="4c3a6-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4c3a6-107">EXAMPLES</span></span>

### <span data-ttu-id="4c3a6-108">Пример 1: Создание свойства, включающего Теги</span><span class="sxs-lookup"><span data-stu-id="4c3a6-108">Example 1: Create a property that includes tags</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$Tags = 'sdk', 'powershell'
PS C:\> New-AzApiManagementProperty -Context $apimContext -PropertyId "Property11" -Name "Property Name" -Value "Property Value" -Tags $Tags
```

<span data-ttu-id="4c3a6-109">Первая команда присваивает переменной $Tags два значения.</span><span class="sxs-lookup"><span data-stu-id="4c3a6-109">The first command assigns two values to the $Tags variable.</span></span>
<span data-ttu-id="4c3a6-110">Вторая команда создает свойство и присваивает строки в $Tags как теги в свойстве.</span><span class="sxs-lookup"><span data-stu-id="4c3a6-110">The second command creates a property and assigns the strings in $Tags as tags on the property.</span></span>

### <span data-ttu-id="4c3a6-111">Пример 2: Создание свойства с секретным значением</span><span class="sxs-lookup"><span data-stu-id="4c3a6-111">Example 2: Create a property that has a secret value</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementProperty -Context $apimContext -PropertyId "Property12" -Name "Secret Property" -Value "Secret Property Value" -Secret
```

<span data-ttu-id="4c3a6-112">Эта команда создает **свойство** с зашифрованным значением.</span><span class="sxs-lookup"><span data-stu-id="4c3a6-112">This command creates a **Property** that has a value that is encrypted.</span></span>

## <span data-ttu-id="4c3a6-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4c3a6-113">PARAMETERS</span></span>

### <span data-ttu-id="4c3a6-114">-Context</span><span class="sxs-lookup"><span data-stu-id="4c3a6-114">-Context</span></span>
<span data-ttu-id="4c3a6-115">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="4c3a6-115">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4c3a6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c3a6-116">-DefaultProfile</span></span>
<span data-ttu-id="4c3a6-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4c3a6-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4c3a6-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4c3a6-118">-Name</span></span>
<span data-ttu-id="4c3a6-119">Указывает имя свойства, создаваемого этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="4c3a6-119">Specifies the name of the property that this cmdlet creates.</span></span>
<span data-ttu-id="4c3a6-120">Максимальная длина — 100 символов.</span><span class="sxs-lookup"><span data-stu-id="4c3a6-120">Maximum length is 100 characters.</span></span>
<span data-ttu-id="4c3a6-121">Имена содержат только буквы, цифры, точки, тире и знаки подчеркивания.</span><span class="sxs-lookup"><span data-stu-id="4c3a6-121">Names contain only letters, digits, period, dash, and underscore characters.</span></span>

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

### <span data-ttu-id="4c3a6-122">-PropertyId</span><span class="sxs-lookup"><span data-stu-id="4c3a6-122">-PropertyId</span></span>
<span data-ttu-id="4c3a6-123">Задает идентификатор для свойства.</span><span class="sxs-lookup"><span data-stu-id="4c3a6-123">Specifies an ID for the property.</span></span>
<span data-ttu-id="4c3a6-124">Максимальная длина — 256 символов.</span><span class="sxs-lookup"><span data-stu-id="4c3a6-124">Maximum length is 256 characters.</span></span>
<span data-ttu-id="4c3a6-125">Если идентификатор не указан, этот командлет создаст его.</span><span class="sxs-lookup"><span data-stu-id="4c3a6-125">If you do not specify an ID, this cmdlet generates one.</span></span>

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

### <span data-ttu-id="4c3a6-126">-Secret (секретный)</span><span class="sxs-lookup"><span data-stu-id="4c3a6-126">-Secret</span></span>
<span data-ttu-id="4c3a6-127">Указывает на то, что значение свойства является секретным и должно быть зашифровано.</span><span class="sxs-lookup"><span data-stu-id="4c3a6-127">Indicates that the property value is a secret and should be encrypted.</span></span>

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

### <span data-ttu-id="4c3a6-128">-Тег</span><span class="sxs-lookup"><span data-stu-id="4c3a6-128">-Tag</span></span>
<span data-ttu-id="4c3a6-129">Теги, связанные с свойством.</span><span class="sxs-lookup"><span data-stu-id="4c3a6-129">Tags to be associated with Property.</span></span> <span data-ttu-id="4c3a6-130">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="4c3a6-130">This parameter is optional.</span></span>

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

### <span data-ttu-id="4c3a6-131">-Value (значение)</span><span class="sxs-lookup"><span data-stu-id="4c3a6-131">-Value</span></span>
<span data-ttu-id="4c3a6-132">Задает значение для свойства.</span><span class="sxs-lookup"><span data-stu-id="4c3a6-132">Specifies a value for the property.</span></span>
<span data-ttu-id="4c3a6-133">Это значение может содержать выражения политики.</span><span class="sxs-lookup"><span data-stu-id="4c3a6-133">This value can contain policy expressions.</span></span>
<span data-ttu-id="4c3a6-134">Максимальная длина — 1000 символов.</span><span class="sxs-lookup"><span data-stu-id="4c3a6-134">Maximum length is 1000 characters.</span></span>
<span data-ttu-id="4c3a6-135">Значение не может быть пустым или состоять только из пробелов.</span><span class="sxs-lookup"><span data-stu-id="4c3a6-135">The value may not be empty or consist only of whitespace.</span></span>

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

### <span data-ttu-id="4c3a6-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c3a6-136">CommonParameters</span></span>
<span data-ttu-id="4c3a6-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4c3a6-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c3a6-138">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4c3a6-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c3a6-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4c3a6-139">INPUTS</span></span>

### <span data-ttu-id="4c3a6-140">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="4c3a6-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="4c3a6-141">System. String</span><span class="sxs-lookup"><span data-stu-id="4c3a6-141">System.String</span></span>

### <span data-ttu-id="4c3a6-142">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="4c3a6-142">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="4c3a6-143">System. String []</span><span class="sxs-lookup"><span data-stu-id="4c3a6-143">System.String[]</span></span>

## <span data-ttu-id="4c3a6-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4c3a6-144">OUTPUTS</span></span>

### <span data-ttu-id="4c3a6-145">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="4c3a6-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProperty</span></span>

## <span data-ttu-id="4c3a6-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="4c3a6-146">NOTES</span></span>

## <span data-ttu-id="4c3a6-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4c3a6-147">RELATED LINKS</span></span>

[<span data-ttu-id="4c3a6-148">Remove-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="4c3a6-148">Remove-AzApiManagementProperty</span></span>](./Remove-AzApiManagementProperty.md)

[<span data-ttu-id="4c3a6-149">Set-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="4c3a6-149">Set-AzApiManagementProperty</span></span>](./Set-AzApiManagementProperty.md)


