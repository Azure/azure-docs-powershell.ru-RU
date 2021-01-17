---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/add-azapimanagementapitogateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementApiToGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementApiToGateway.md
ms.openlocfilehash: 6bb40d46c80e609824b1c56d05091ade5716f7f8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98401420"
---
# <span data-ttu-id="dc76c-101">Add-AzApiManagementApiToGateway</span><span class="sxs-lookup"><span data-stu-id="dc76c-101">Add-AzApiManagementApiToGateway</span></span>

## <span data-ttu-id="dc76c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dc76c-102">SYNOPSIS</span></span>
<span data-ttu-id="dc76c-103">Прикрепит API к шлюзу.</span><span class="sxs-lookup"><span data-stu-id="dc76c-103">Attaches an API to a gateway.</span></span>

## <span data-ttu-id="dc76c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="dc76c-104">SYNTAX</span></span>

```
Add-AzApiManagementApiToGateway -Context <PsApiManagementContext> -GatewayId <String> -ApiId <String>
 [-ProvisioningState <PsApiManagementGatewayApiProvisioningState>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dc76c-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dc76c-105">DESCRIPTION</span></span>
<span data-ttu-id="dc76c-106">**Cmdlet Add-AzApiManagementApiToGateway** добавляет К шлюзу API управления Azure API.</span><span class="sxs-lookup"><span data-stu-id="dc76c-106">The **Add-AzApiManagementApiToGateway** cmdlet adds an Azure API Management API to a Gateway.</span></span>

## <span data-ttu-id="dc76c-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="dc76c-107">EXAMPLES</span></span>

### <span data-ttu-id="dc76c-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="dc76c-108">Example 1</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Add-AzApiManagementApiToGateway -Context $ApiMgmtContext -GatewayId "0123456789" -ApiId "0001"
```

<span data-ttu-id="dc76c-109">Эта команда добавляет указанный API к указанному шлюзу.</span><span class="sxs-lookup"><span data-stu-id="dc76c-109">This command adds the specified API to the specified Gateway.</span></span>

## <span data-ttu-id="dc76c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dc76c-110">PARAMETERS</span></span>

### <span data-ttu-id="dc76c-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="dc76c-111">-ApiId</span></span>
<span data-ttu-id="dc76c-112">Идентификатор существующего API.</span><span class="sxs-lookup"><span data-stu-id="dc76c-112">Identifier of existing API.</span></span>
<span data-ttu-id="dc76c-113">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="dc76c-113">This parameter is required.</span></span>

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

### <span data-ttu-id="dc76c-114">-Контекст</span><span class="sxs-lookup"><span data-stu-id="dc76c-114">-Context</span></span>
<span data-ttu-id="dc76c-115">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="dc76c-115">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="dc76c-116">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="dc76c-116">This parameter is required.</span></span>

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

### <span data-ttu-id="dc76c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc76c-117">-DefaultProfile</span></span>
<span data-ttu-id="dc76c-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dc76c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dc76c-119">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="dc76c-119">-GatewayId</span></span>
<span data-ttu-id="dc76c-120">Идентификатор существующего шлюза.</span><span class="sxs-lookup"><span data-stu-id="dc76c-120">Identifier of existing gateway.</span></span>
<span data-ttu-id="dc76c-121">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="dc76c-121">This parameter is required.</span></span>

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

### <span data-ttu-id="dc76c-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dc76c-122">-PassThru</span></span>
<span data-ttu-id="dc76c-123">Если этот задан, будет указано "Истина" в случае успешной операции.</span><span class="sxs-lookup"><span data-stu-id="dc76c-123">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="dc76c-124">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="dc76c-124">This parameter is optional.</span></span>
<span data-ttu-id="dc76c-125">Значение по умолчанию — false.</span><span class="sxs-lookup"><span data-stu-id="dc76c-125">Default value is false.</span></span>

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

### <span data-ttu-id="dc76c-126">-ProvisioningState</span><span class="sxs-lookup"><span data-stu-id="dc76c-126">-ProvisioningState</span></span>
<span data-ttu-id="dc76c-127">Состояние подготовка (создано).</span><span class="sxs-lookup"><span data-stu-id="dc76c-127">Provisioning State (Created).</span></span>
<span data-ttu-id="dc76c-128">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="dc76c-128">This parameter is optional.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayApiProvisioningState]
Parameter Sets: (All)
Aliases:
Accepted values: Created

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc76c-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dc76c-129">-Confirm</span></span>
<span data-ttu-id="dc76c-130">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="dc76c-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc76c-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc76c-131">-WhatIf</span></span>
<span data-ttu-id="dc76c-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dc76c-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dc76c-133">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="dc76c-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dc76c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc76c-134">CommonParameters</span></span>
<span data-ttu-id="dc76c-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc76c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc76c-136">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dc76c-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc76c-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dc76c-137">INPUTS</span></span>

### <span data-ttu-id="dc76c-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="dc76c-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="dc76c-139">System.String</span><span class="sxs-lookup"><span data-stu-id="dc76c-139">System.String</span></span>

### <span data-ttu-id="dc76c-140">System.Nullable'1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayApiProvisioningState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=2.0.1.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="dc76c-140">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayApiProvisioningState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=2.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="dc76c-141">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="dc76c-141">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="dc76c-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="dc76c-142">OUTPUTS</span></span>

### <span data-ttu-id="dc76c-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="dc76c-143">System.Boolean</span></span>

## <span data-ttu-id="dc76c-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="dc76c-144">NOTES</span></span>

## <span data-ttu-id="dc76c-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dc76c-145">RELATED LINKS</span></span>

[<span data-ttu-id="dc76c-146">Remove-AzApiManagementApiFromGateway</span><span class="sxs-lookup"><span data-stu-id="dc76c-146">Remove-AzApiManagementApiFromGateway</span></span>](./Remove-AzApiManagementApiFromGateway.md)