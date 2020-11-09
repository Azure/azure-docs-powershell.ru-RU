---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementnamedvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementNamedValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementNamedValue.md
ms.openlocfilehash: 08e29c91e253c648b774e56d7e236accdd5fbff0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246929"
---
# <span data-ttu-id="e9687-101">New-AzApiManagementNamedValue</span><span class="sxs-lookup"><span data-stu-id="e9687-101">New-AzApiManagementNamedValue</span></span>

## <span data-ttu-id="e9687-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e9687-102">SYNOPSIS</span></span>
<span data-ttu-id="e9687-103">Создание нового именованного значения.</span><span class="sxs-lookup"><span data-stu-id="e9687-103">Creates new Named Value.</span></span>

## <span data-ttu-id="e9687-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e9687-104">SYNTAX</span></span>

```
New-AzApiManagementNamedValue -Context <PsApiManagementContext> [-NamedValueId <String>] -Name <String>
 -Value <String> [-Secret] [-Tag <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e9687-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e9687-105">DESCRIPTION</span></span>
<span data-ttu-id="e9687-106">Командлет **New-AzApiManagementNamedValue** создает элемент управления API Azure **с именем value**.</span><span class="sxs-lookup"><span data-stu-id="e9687-106">The **New-AzApiManagementNamedValue** cmdlet creates an Azure API Management **Named Value**.</span></span>

## <span data-ttu-id="e9687-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e9687-107">EXAMPLES</span></span>

### <span data-ttu-id="e9687-108">Пример 1: Создание именованного значения, включающего Теги</span><span class="sxs-lookup"><span data-stu-id="e9687-108">Example 1: Create a named value that includes tags</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$Tags = 'sdk', 'powershell'
PS C:\> New-AzApiManagementNamedValue -Context $apimContext -NamedValueId "Property11" -Name "Property Name" -Value "Property Value" -Tags $Tags
```

<span data-ttu-id="e9687-109">Первая команда присваивает переменной $Tags два значения.</span><span class="sxs-lookup"><span data-stu-id="e9687-109">The first command assigns two values to the $Tags variable.</span></span>
<span data-ttu-id="e9687-110">Вторая команда создает именованное значение и назначает строки в $Tags в качестве тегов в свойстве.</span><span class="sxs-lookup"><span data-stu-id="e9687-110">The second command creates a named value and assigns the strings in $Tags as tags on the property.</span></span>

### <span data-ttu-id="e9687-111">Пример 2: Создание именованного значения с секретным значением</span><span class="sxs-lookup"><span data-stu-id="e9687-111">Example 2: Create a named value that has a secret value</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementNamedValue -Context $apimContext -NamedValueId "Property12" -Name "Secret Property" -Value "Secret Property Value" -Secret
```

<span data-ttu-id="e9687-112">Эта команда создает **именованное значение** , которое имеет зашифрованное значение.</span><span class="sxs-lookup"><span data-stu-id="e9687-112">This command creates a **Named Value** that has a value that is encrypted.</span></span>

## <span data-ttu-id="e9687-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e9687-113">PARAMETERS</span></span>

### <span data-ttu-id="e9687-114">-Context</span><span class="sxs-lookup"><span data-stu-id="e9687-114">-Context</span></span>
<span data-ttu-id="e9687-115">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="e9687-115">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="e9687-116">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="e9687-116">This parameter is required.</span></span>

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

### <span data-ttu-id="e9687-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9687-117">-DefaultProfile</span></span>
<span data-ttu-id="e9687-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e9687-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e9687-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e9687-119">-Name</span></span>
<span data-ttu-id="e9687-120">Имя именованного значения.</span><span class="sxs-lookup"><span data-stu-id="e9687-120">Name of the named value.</span></span>
<span data-ttu-id="e9687-121">Максимальная длина — 100 символов.</span><span class="sxs-lookup"><span data-stu-id="e9687-121">Maximum length is 100 characters.</span></span>
<span data-ttu-id="e9687-122">Оно может содержать только буквы, цифры, точки, тире и знаки подчеркивания.</span><span class="sxs-lookup"><span data-stu-id="e9687-122">It may contain only letters, digits, period, dash, and underscore characters.</span></span>
<span data-ttu-id="e9687-123">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="e9687-123">This parameter is required.</span></span>

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

### <span data-ttu-id="e9687-124">-NamedValueId</span><span class="sxs-lookup"><span data-stu-id="e9687-124">-NamedValueId</span></span>
<span data-ttu-id="e9687-125">Идентификатор нового именованного значения.</span><span class="sxs-lookup"><span data-stu-id="e9687-125">Identifier of new named value.</span></span>
<span data-ttu-id="e9687-126">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="e9687-126">This parameter is optional.</span></span>
<span data-ttu-id="e9687-127">Если не указано, будет создано.</span><span class="sxs-lookup"><span data-stu-id="e9687-127">If not specified will be generated.</span></span>

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

### <span data-ttu-id="e9687-128">-Secret (секретный)</span><span class="sxs-lookup"><span data-stu-id="e9687-128">-Secret</span></span>
<span data-ttu-id="e9687-129">Определяет, является ли значение секретным, которое должно быть зашифровано.</span><span class="sxs-lookup"><span data-stu-id="e9687-129">Determines whether the value is a secret and should be encrypted or not.</span></span>
<span data-ttu-id="e9687-130">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="e9687-130">This parameter is optional.</span></span>
<span data-ttu-id="e9687-131">Значение по умолчанию — false.</span><span class="sxs-lookup"><span data-stu-id="e9687-131">Default Value is false.</span></span>

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

### <span data-ttu-id="e9687-132">-Тег</span><span class="sxs-lookup"><span data-stu-id="e9687-132">-Tag</span></span>
<span data-ttu-id="e9687-133">Теги, которые должны быть связаны с именованным значением.</span><span class="sxs-lookup"><span data-stu-id="e9687-133">Tags to be associated with named value.</span></span>
<span data-ttu-id="e9687-134">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="e9687-134">This parameter is optional.</span></span>

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

### <span data-ttu-id="e9687-135">-Value (значение)</span><span class="sxs-lookup"><span data-stu-id="e9687-135">-Value</span></span>
<span data-ttu-id="e9687-136">Значение именованного значения.</span><span class="sxs-lookup"><span data-stu-id="e9687-136">Value of the named value.</span></span>
<span data-ttu-id="e9687-137">Может содержать выражения политики.</span><span class="sxs-lookup"><span data-stu-id="e9687-137">Can contain policy expressions.</span></span>
<span data-ttu-id="e9687-138">Максимальная длина — 1000 символов.</span><span class="sxs-lookup"><span data-stu-id="e9687-138">Maximum length is 1000 characters.</span></span>
<span data-ttu-id="e9687-139">Оно не может быть пустым или состоять только из пробелов.</span><span class="sxs-lookup"><span data-stu-id="e9687-139">It may not be empty or consist only of whitespace.</span></span>
<span data-ttu-id="e9687-140">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="e9687-140">This parameter is required.</span></span>

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

### <span data-ttu-id="e9687-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e9687-141">-Confirm</span></span>
<span data-ttu-id="e9687-142">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e9687-142">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9687-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9687-143">-WhatIf</span></span>
<span data-ttu-id="e9687-144">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e9687-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e9687-145">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e9687-145">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9687-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9687-146">CommonParameters</span></span>
<span data-ttu-id="e9687-147">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e9687-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9687-148">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e9687-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9687-149">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e9687-149">INPUTS</span></span>

### <span data-ttu-id="e9687-150">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="e9687-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="e9687-151">System. String</span><span class="sxs-lookup"><span data-stu-id="e9687-151">System.String</span></span>

### <span data-ttu-id="e9687-152">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="e9687-152">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="e9687-153">System. String []</span><span class="sxs-lookup"><span data-stu-id="e9687-153">System.String[]</span></span>

## <span data-ttu-id="e9687-154">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e9687-154">OUTPUTS</span></span>

### <span data-ttu-id="e9687-155">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementNamedValue</span><span class="sxs-lookup"><span data-stu-id="e9687-155">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementNamedValue</span></span>

## <span data-ttu-id="e9687-156">Пуск</span><span class="sxs-lookup"><span data-stu-id="e9687-156">NOTES</span></span>

## <span data-ttu-id="e9687-157">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e9687-157">RELATED LINKS</span></span>