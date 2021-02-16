---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementgatewayhostnameconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementGatewayHostnameConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementGatewayHostnameConfiguration.md
ms.openlocfilehash: e1999387cc2beb5a55fba3aef771a76440804f22
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100212113"
---
# <span data-ttu-id="c690c-101">Remove-AzApiManagementGatewayHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="c690c-101">Remove-AzApiManagementGatewayHostnameConfiguration</span></span>

## <span data-ttu-id="c690c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c690c-102">SYNOPSIS</span></span>
<span data-ttu-id="c690c-103">Удаляет конфигурацию имени пользователя из существующего шлюза.</span><span class="sxs-lookup"><span data-stu-id="c690c-103">Removes a hostname configuration from the existing Gateway.</span></span>

## <span data-ttu-id="c690c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c690c-104">SYNTAX</span></span>

### <span data-ttu-id="c690c-105">ContextParameterSetName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c690c-105">ContextParameterSetName (Default)</span></span>
```
Remove-AzApiManagementGatewayHostnameConfiguration -Context <PsApiManagementContext> -GatewayId <String>
 -GatewayHostnameConfigurationId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c690c-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c690c-106">ByInputObjectParameterSet</span></span>
```
Remove-AzApiManagementGatewayHostnameConfiguration -InputObject <PsApiManagementGatewayHostnameConfiguration>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c690c-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c690c-107">ByResourceIdParameterSet</span></span>
```
Remove-AzApiManagementGatewayHostnameConfiguration -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c690c-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c690c-108">DESCRIPTION</span></span>
<span data-ttu-id="c690c-109">Из существующего шлюза удаляется конфигурация имени пользователя **AzApiManagementGatewayHostnameConfiguration.**</span><span class="sxs-lookup"><span data-stu-id="c690c-109">The **Remove-AzApiManagementGatewayHostnameConfiguration** cmdlet removes a hostname configuration from the existing Gateway.</span></span>

## <span data-ttu-id="c690c-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c690c-110">EXAMPLES</span></span>

### <span data-ttu-id="c690c-111">Пример 1. Удаление существующей конфигурации имени шлюза</span><span class="sxs-lookup"><span data-stu-id="c690c-111">Example 1: Remove an existing gateway hostname configuration</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementGatewayHostnameConfiguration -Context $apimContext -GatewayId "g0001" -GatewayHostnameConfigurationId "h0001" -Force
```

<span data-ttu-id="c690c-112">Эта команда удаляет существующую конфигурацию имени шлюза и не запросит подтверждение.</span><span class="sxs-lookup"><span data-stu-id="c690c-112">This command removes an existing gateway hostname configuration and does not prompt the user for confirmation.</span></span>

## <span data-ttu-id="c690c-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c690c-113">PARAMETERS</span></span>

### <span data-ttu-id="c690c-114">-Контекст</span><span class="sxs-lookup"><span data-stu-id="c690c-114">-Context</span></span>
<span data-ttu-id="c690c-115">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="c690c-115">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="c690c-116">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="c690c-116">This parameter is required.</span></span>

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

### <span data-ttu-id="c690c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c690c-117">-DefaultProfile</span></span>
<span data-ttu-id="c690c-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c690c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c690c-119">-GatewayHostnameConfigurationId</span><span class="sxs-lookup"><span data-stu-id="c690c-119">-GatewayHostnameConfigurationId</span></span>
<span data-ttu-id="c690c-120">Идентификатор существующей конфигурации имени шлюза.</span><span class="sxs-lookup"><span data-stu-id="c690c-120">Identifier of existing gateway hostname configuration.</span></span>
<span data-ttu-id="c690c-121">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="c690c-121">This parameter is required.</span></span>

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

### <span data-ttu-id="c690c-122">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="c690c-122">-GatewayId</span></span>
<span data-ttu-id="c690c-123">Идентификатор существующего шлюза.</span><span class="sxs-lookup"><span data-stu-id="c690c-123">Identifier of existing gateway.</span></span>
<span data-ttu-id="c690c-124">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="c690c-124">This parameter is required.</span></span>

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

### <span data-ttu-id="c690c-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c690c-125">-InputObject</span></span>
<span data-ttu-id="c690c-126">Экземпляр PsApiManagementGatewayHostnameConfiguration.</span><span class="sxs-lookup"><span data-stu-id="c690c-126">Instance of PsApiManagementGatewayHostnameConfiguration.</span></span> <span data-ttu-id="c690c-127">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="c690c-127">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayHostnameConfiguration
Parameter Sets: ByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c690c-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c690c-128">-PassThru</span></span>
<span data-ttu-id="c690c-129">Если этот задан, будет указано "Истина" в случае успешной операции.</span><span class="sxs-lookup"><span data-stu-id="c690c-129">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="c690c-130">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="c690c-130">This parameter is optional.</span></span>
<span data-ttu-id="c690c-131">Значение по умолчанию — false.</span><span class="sxs-lookup"><span data-stu-id="c690c-131">Default value is false.</span></span>

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

### <span data-ttu-id="c690c-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c690c-132">-ResourceId</span></span>
<span data-ttu-id="c690c-133">Arm ResourceId шлюзаHostnameConfiguration.</span><span class="sxs-lookup"><span data-stu-id="c690c-133">Arm ResourceId of the GatewayHostnameConfiguration.</span></span> <span data-ttu-id="c690c-134">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="c690c-134">This parameter is required.</span></span>

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

### <span data-ttu-id="c690c-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c690c-135">-Confirm</span></span>
<span data-ttu-id="c690c-136">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="c690c-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c690c-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c690c-137">-WhatIf</span></span>
<span data-ttu-id="c690c-138">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c690c-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c690c-139">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="c690c-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c690c-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c690c-140">CommonParameters</span></span>
<span data-ttu-id="c690c-141">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c690c-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c690c-142">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c690c-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c690c-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c690c-143">INPUTS</span></span>

### <span data-ttu-id="c690c-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="c690c-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="c690c-145">System.String</span><span class="sxs-lookup"><span data-stu-id="c690c-145">System.String</span></span>

### <span data-ttu-id="c690c-146">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="c690c-146">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="c690c-147">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c690c-147">OUTPUTS</span></span>

### <span data-ttu-id="c690c-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c690c-148">System.Boolean</span></span>

## <span data-ttu-id="c690c-149">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c690c-149">NOTES</span></span>

## <span data-ttu-id="c690c-150">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c690c-150">RELATED LINKS</span></span>
