---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApiVersionSet.md
ms.openlocfilehash: 4ff48709b02cdd0270c559ea8be2f4e269dbce2f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93731994"
---
# <span data-ttu-id="7072c-101">Remove-AzureRmApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="7072c-101">Remove-AzureRmApiManagementApiVersionSet</span></span>

## <span data-ttu-id="7072c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7072c-102">SYNOPSIS</span></span>
<span data-ttu-id="7072c-103">Удаляет определенный набор версий API</span><span class="sxs-lookup"><span data-stu-id="7072c-103">Removes a particular Api Version Set</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7072c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7072c-104">SYNTAX</span></span>

### <span data-ttu-id="7072c-105">ExpandedParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7072c-105">ExpandedParameter (Default)</span></span>
```
Remove-AzureRmApiManagementApiVersionSet -Context <PsApiManagementContext> -ApiVersionSetId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7072c-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="7072c-106">ByInputObject</span></span>
```
Remove-AzureRmApiManagementApiVersionSet -InputObject <PsApiManagementApiVersionSet> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7072c-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7072c-107">DESCRIPTION</span></span>

<span data-ttu-id="7072c-108">Командлет **Remove-AzureRmApiManagementApiVersionSet** удаляет существующий наборы API.</span><span class="sxs-lookup"><span data-stu-id="7072c-108">The **Remove-AzureRmApiManagementApiVersionSet** cmdlet removes an existing API Version Set.</span></span>

## <span data-ttu-id="7072c-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7072c-109">EXAMPLES</span></span>

### <span data-ttu-id="7072c-110">Пример 1: Удаление множества версий API</span><span class="sxs-lookup"><span data-stu-id="7072c-110">Example 1: Remove an API Version set</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementApiVersionSet -Context $apimContext -ApiVersionSetId "query-param-set"
```

<span data-ttu-id="7072c-111">Эта команда удаляет версию API, установленную с указанным ApiVersionSetId.</span><span class="sxs-lookup"><span data-stu-id="7072c-111">This command removes the API Version Set with the specified ApiVersionSetId.</span></span>

## <span data-ttu-id="7072c-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7072c-112">PARAMETERS</span></span>

### <span data-ttu-id="7072c-113">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="7072c-113">-ApiVersionSetId</span></span>
<span data-ttu-id="7072c-114">Идентификатор набора версий API.</span><span class="sxs-lookup"><span data-stu-id="7072c-114">Identifier of the API Version Set.</span></span>
<span data-ttu-id="7072c-115">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="7072c-115">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7072c-116">-Context</span><span class="sxs-lookup"><span data-stu-id="7072c-116">-Context</span></span>
<span data-ttu-id="7072c-117">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="7072c-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="7072c-118">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="7072c-118">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7072c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7072c-119">-DefaultProfile</span></span>
<span data-ttu-id="7072c-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7072c-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7072c-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7072c-121">-InputObject</span></span>
<span data-ttu-id="7072c-122">Экземпляр PsApiManagementApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="7072c-122">Instance of PsApiManagementApiVersionSet.</span></span> <span data-ttu-id="7072c-123">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="7072c-123">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7072c-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7072c-124">-PassThru</span></span>
<span data-ttu-id="7072c-125">Если задано значение true, операция Case запишется успешно.</span><span class="sxs-lookup"><span data-stu-id="7072c-125">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="7072c-126">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="7072c-126">This parameter is optional.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7072c-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7072c-127">-Confirm</span></span>
<span data-ttu-id="7072c-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7072c-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7072c-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7072c-129">-WhatIf</span></span>
<span data-ttu-id="7072c-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7072c-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7072c-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7072c-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7072c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7072c-132">CommonParameters</span></span>
<span data-ttu-id="7072c-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7072c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7072c-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7072c-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7072c-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7072c-135">INPUTS</span></span>

### <span data-ttu-id="7072c-136">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="7072c-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>
<span data-ttu-id="7072c-137">Параметры: Context (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7072c-137">Parameters: Context (ByValue)</span></span>

### <span data-ttu-id="7072c-138">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="7072c-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>
<span data-ttu-id="7072c-139">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7072c-139">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="7072c-140">System. String</span><span class="sxs-lookup"><span data-stu-id="7072c-140">System.String</span></span>

## <span data-ttu-id="7072c-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7072c-141">OUTPUTS</span></span>

### <span data-ttu-id="7072c-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7072c-142">System.Boolean</span></span>

## <span data-ttu-id="7072c-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="7072c-143">NOTES</span></span>

## <span data-ttu-id="7072c-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7072c-144">RELATED LINKS</span></span>

[<span data-ttu-id="7072c-145">Get-AzureRmApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="7072c-145">Get-AzureRmApiManagementApiVersionSet</span></span>](./Get-AzureRmApiManagementApiVersionSet.md)

[<span data-ttu-id="7072c-146">New-AzureRmApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="7072c-146">New-AzureRmApiManagementApiVersionSet</span></span>](./New-AzureRmApiManagementApiVersionSet.md)

[<span data-ttu-id="7072c-147">Set-AzureRmApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="7072c-147">Set-AzureRmApiManagementApiVersionSet</span></span>](./Set-AzureRmApiManagementApiVersionSet.md)
