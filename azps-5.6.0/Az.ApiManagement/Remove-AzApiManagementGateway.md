---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagementgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementGateway.md
ms.openlocfilehash: 2ccd68fb5c1028408771e3011642797c8125ace3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994524"
---
# <span data-ttu-id="c65bb-101">Remove-AzApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="c65bb-101">Remove-AzApiManagementGateway</span></span>

## <span data-ttu-id="c65bb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c65bb-102">SYNOPSIS</span></span>
<span data-ttu-id="c65bb-103">Отсоединяет API от шлюза.</span><span class="sxs-lookup"><span data-stu-id="c65bb-103">Detaches an API from a Gateway.</span></span>

## <span data-ttu-id="c65bb-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c65bb-104">SYNTAX</span></span>

### <span data-ttu-id="c65bb-105">ContextParameterSetName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c65bb-105">ContextParameterSetName (Default)</span></span>
```
Remove-AzApiManagementGateway -Context <PsApiManagementContext> -GatewayId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c65bb-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c65bb-106">ByInputObjectParameterSet</span></span>
```
Remove-AzApiManagementGateway -InputObject <PsApiManagementGateway> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c65bb-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c65bb-107">ByResourceIdParameterSet</span></span>
```
Remove-AzApiManagementGateway -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c65bb-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c65bb-108">DESCRIPTION</span></span>
<span data-ttu-id="c65bb-109">**Cmdlet Remove-AzApiManagementGateway** отсоединяет API от шлюза.</span><span class="sxs-lookup"><span data-stu-id="c65bb-109">The **Remove-AzApiManagementGateway** cmdlet detaches an API from a Gateway.</span></span>

## <span data-ttu-id="c65bb-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c65bb-110">EXAMPLES</span></span>

### <span data-ttu-id="c65bb-111">Пример 1. Удаление существующего шлюза</span><span class="sxs-lookup"><span data-stu-id="c65bb-111">Example 1: Remove an existing gateway</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementGateway -Context $apimContext -GatewayId "g0001" -Force
```

<span data-ttu-id="c65bb-112">Эта команда удаляет существующий шлюз и не выбирает у пользователя подтверждение.</span><span class="sxs-lookup"><span data-stu-id="c65bb-112">This command removes an existing gateway and does not prompt the user for confirmation.</span></span>

## <span data-ttu-id="c65bb-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c65bb-113">PARAMETERS</span></span>

### <span data-ttu-id="c65bb-114">-Контекст</span><span class="sxs-lookup"><span data-stu-id="c65bb-114">-Context</span></span>
<span data-ttu-id="c65bb-115">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="c65bb-115">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="c65bb-116">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="c65bb-116">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ContextParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c65bb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c65bb-117">-DefaultProfile</span></span>
<span data-ttu-id="c65bb-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c65bb-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c65bb-119">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="c65bb-119">-GatewayId</span></span>
<span data-ttu-id="c65bb-120">Идентификатор существующего шлюза.</span><span class="sxs-lookup"><span data-stu-id="c65bb-120">Identifier of existing gateway.</span></span>
<span data-ttu-id="c65bb-121">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="c65bb-121">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c65bb-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c65bb-122">-InputObject</span></span>
<span data-ttu-id="c65bb-123">Экземпляр PsApiManagementGateway.</span><span class="sxs-lookup"><span data-stu-id="c65bb-123">Instance of PsApiManagementGateway.</span></span> <span data-ttu-id="c65bb-124">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="c65bb-124">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway
Parameter Sets: ByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c65bb-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c65bb-125">-PassThru</span></span>
<span data-ttu-id="c65bb-126">Если этот задан, будет указано "Истина" в случае успешной операции.</span><span class="sxs-lookup"><span data-stu-id="c65bb-126">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="c65bb-127">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="c65bb-127">This parameter is optional.</span></span>
<span data-ttu-id="c65bb-128">Значение по умолчанию — false.</span><span class="sxs-lookup"><span data-stu-id="c65bb-128">Default value is false.</span></span>

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

### <span data-ttu-id="c65bb-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c65bb-129">-ResourceId</span></span>
<span data-ttu-id="c65bb-130">Arm ResourceId шлюза.</span><span class="sxs-lookup"><span data-stu-id="c65bb-130">Arm ResourceId of the Gateway.</span></span> <span data-ttu-id="c65bb-131">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="c65bb-131">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c65bb-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c65bb-132">-Confirm</span></span>
<span data-ttu-id="c65bb-133">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c65bb-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c65bb-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c65bb-134">-WhatIf</span></span>
<span data-ttu-id="c65bb-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c65bb-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c65bb-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="c65bb-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c65bb-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c65bb-137">CommonParameters</span></span>
<span data-ttu-id="c65bb-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c65bb-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c65bb-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c65bb-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c65bb-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c65bb-140">INPUTS</span></span>

### <span data-ttu-id="c65bb-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="c65bb-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="c65bb-142">System.String</span><span class="sxs-lookup"><span data-stu-id="c65bb-142">System.String</span></span>

### <span data-ttu-id="c65bb-143">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="c65bb-143">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="c65bb-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c65bb-144">OUTPUTS</span></span>

### <span data-ttu-id="c65bb-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c65bb-145">System.Boolean</span></span>

## <span data-ttu-id="c65bb-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c65bb-146">NOTES</span></span>

## <span data-ttu-id="c65bb-147">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c65bb-147">RELATED LINKS</span></span>
