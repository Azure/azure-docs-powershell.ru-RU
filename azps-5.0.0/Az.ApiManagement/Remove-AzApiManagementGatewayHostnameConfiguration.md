---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementgatewayhostnameconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementGatewayHostnameConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementGatewayHostnameConfiguration.md
ms.openlocfilehash: e1999387cc2beb5a55fba3aef771a76440804f22
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248152"
---
# <span data-ttu-id="6f466-101">Remove-AzApiManagementGatewayHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="6f466-101">Remove-AzApiManagementGatewayHostnameConfiguration</span></span>

## <span data-ttu-id="6f466-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6f466-102">SYNOPSIS</span></span>
<span data-ttu-id="6f466-103">Удаление конфигурации hostname из существующего шлюза.</span><span class="sxs-lookup"><span data-stu-id="6f466-103">Removes a hostname configuration from the existing Gateway.</span></span>

## <span data-ttu-id="6f466-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6f466-104">SYNTAX</span></span>

### <span data-ttu-id="6f466-105">ContextParameterSetName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6f466-105">ContextParameterSetName (Default)</span></span>
```
Remove-AzApiManagementGatewayHostnameConfiguration -Context <PsApiManagementContext> -GatewayId <String>
 -GatewayHostnameConfigurationId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f466-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6f466-106">ByInputObjectParameterSet</span></span>
```
Remove-AzApiManagementGatewayHostnameConfiguration -InputObject <PsApiManagementGatewayHostnameConfiguration>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f466-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6f466-107">ByResourceIdParameterSet</span></span>
```
Remove-AzApiManagementGatewayHostnameConfiguration -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6f466-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6f466-108">DESCRIPTION</span></span>
<span data-ttu-id="6f466-109">Командлет **Remove-AzApiManagementGatewayHostnameConfiguration** удаляет конфигурацию hostname из существующего шлюза.</span><span class="sxs-lookup"><span data-stu-id="6f466-109">The **Remove-AzApiManagementGatewayHostnameConfiguration** cmdlet removes a hostname configuration from the existing Gateway.</span></span>

## <span data-ttu-id="6f466-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6f466-110">EXAMPLES</span></span>

### <span data-ttu-id="6f466-111">Пример 1: удаление существующей конфигурации hostname Gateway</span><span class="sxs-lookup"><span data-stu-id="6f466-111">Example 1: Remove an existing gateway hostname configuration</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementGatewayHostnameConfiguration -Context $apimContext -GatewayId "g0001" -GatewayHostnameConfigurationId "h0001" -Force
```

<span data-ttu-id="6f466-112">Эта команда удаляет существующую конфигурацию hostname Gateway и не запрашивает подтверждение у пользователя.</span><span class="sxs-lookup"><span data-stu-id="6f466-112">This command removes an existing gateway hostname configuration and does not prompt the user for confirmation.</span></span>

## <span data-ttu-id="6f466-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6f466-113">PARAMETERS</span></span>

### <span data-ttu-id="6f466-114">-Context</span><span class="sxs-lookup"><span data-stu-id="6f466-114">-Context</span></span>
<span data-ttu-id="6f466-115">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="6f466-115">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="6f466-116">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="6f466-116">This parameter is required.</span></span>

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

### <span data-ttu-id="6f466-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f466-117">-DefaultProfile</span></span>
<span data-ttu-id="6f466-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6f466-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6f466-119">-GatewayHostnameConfigurationId</span><span class="sxs-lookup"><span data-stu-id="6f466-119">-GatewayHostnameConfigurationId</span></span>
<span data-ttu-id="6f466-120">Идентификатор существующей конфигурации hostname Gateway.</span><span class="sxs-lookup"><span data-stu-id="6f466-120">Identifier of existing gateway hostname configuration.</span></span>
<span data-ttu-id="6f466-121">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="6f466-121">This parameter is required.</span></span>

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

### <span data-ttu-id="6f466-122">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="6f466-122">-GatewayId</span></span>
<span data-ttu-id="6f466-123">Идентификатор существующего шлюза.</span><span class="sxs-lookup"><span data-stu-id="6f466-123">Identifier of existing gateway.</span></span>
<span data-ttu-id="6f466-124">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="6f466-124">This parameter is required.</span></span>

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

### <span data-ttu-id="6f466-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6f466-125">-InputObject</span></span>
<span data-ttu-id="6f466-126">Экземпляр PsApiManagementGatewayHostnameConfiguration.</span><span class="sxs-lookup"><span data-stu-id="6f466-126">Instance of PsApiManagementGatewayHostnameConfiguration.</span></span> <span data-ttu-id="6f466-127">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="6f466-127">This parameter is required.</span></span>

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

### <span data-ttu-id="6f466-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6f466-128">-PassThru</span></span>
<span data-ttu-id="6f466-129">Если задано значение true, операция Case запишется успешно.</span><span class="sxs-lookup"><span data-stu-id="6f466-129">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="6f466-130">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="6f466-130">This parameter is optional.</span></span>
<span data-ttu-id="6f466-131">Значение по умолчанию — false.</span><span class="sxs-lookup"><span data-stu-id="6f466-131">Default value is false.</span></span>

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

### <span data-ttu-id="6f466-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6f466-132">-ResourceId</span></span>
<span data-ttu-id="6f466-133">ИД ResourceId для GatewayHostnameConfiguration.</span><span class="sxs-lookup"><span data-stu-id="6f466-133">Arm ResourceId of the GatewayHostnameConfiguration.</span></span> <span data-ttu-id="6f466-134">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="6f466-134">This parameter is required.</span></span>

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

### <span data-ttu-id="6f466-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6f466-135">-Confirm</span></span>
<span data-ttu-id="6f466-136">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6f466-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6f466-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f466-137">-WhatIf</span></span>
<span data-ttu-id="6f466-138">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="6f466-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6f466-139">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6f466-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6f466-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f466-140">CommonParameters</span></span>
<span data-ttu-id="6f466-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6f466-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f466-142">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6f466-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f466-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6f466-143">INPUTS</span></span>

### <span data-ttu-id="6f466-144">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="6f466-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="6f466-145">System. String</span><span class="sxs-lookup"><span data-stu-id="6f466-145">System.String</span></span>

### <span data-ttu-id="6f466-146">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="6f466-146">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="6f466-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6f466-147">OUTPUTS</span></span>

### <span data-ttu-id="6f466-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6f466-148">System.Boolean</span></span>

## <span data-ttu-id="6f466-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="6f466-149">NOTES</span></span>

## <span data-ttu-id="6f466-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6f466-150">RELATED LINKS</span></span>
