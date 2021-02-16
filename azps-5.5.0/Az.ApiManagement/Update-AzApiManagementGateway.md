---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/Update-AzApiManagementGateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementGateway.md
ms.openlocfilehash: d053bc60390c43c3409bb7adfad5a3ff3720f5b7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100244309"
---
# <span data-ttu-id="c0302-101">Update-AzApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="c0302-101">Update-AzApiManagementGateway</span></span>

## <span data-ttu-id="c0302-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c0302-102">SYNOPSIS</span></span>
<span data-ttu-id="c0302-103">Настраивает шлюз управления API.</span><span class="sxs-lookup"><span data-stu-id="c0302-103">Configures an API management Gateway.</span></span>

## <span data-ttu-id="c0302-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c0302-104">SYNTAX</span></span>

### <span data-ttu-id="c0302-105">ExpandedParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c0302-105">ExpandedParameter (Default)</span></span>
```
Update-AzApiManagementGateway -Context <PsApiManagementContext> -GatewayId <String> [-Description <String>]
 [-LocationData <PsApiManagementResourceLocation>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0302-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="c0302-106">ByInputObject</span></span>
```
Update-AzApiManagementGateway -InputObject <PsApiManagementGateway> [-Description <String>]
 [-LocationData <PsApiManagementResourceLocation>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0302-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="c0302-107">ByResourceId</span></span>
```
Update-AzApiManagementGateway -ResourceId <String> [-Description <String>]
 [-LocationData <PsApiManagementResourceLocation>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0302-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c0302-108">DESCRIPTION</span></span>
<span data-ttu-id="c0302-109">Для настройки шлюза управления API будет настроен **cmdlet Update-AzApiManagementGateway.**</span><span class="sxs-lookup"><span data-stu-id="c0302-109">The **Update-AzApiManagementGateway** cmdlet configures an API management Gateway.</span></span>

## <span data-ttu-id="c0302-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c0302-110">EXAMPLES</span></span>

### <span data-ttu-id="c0302-111">Пример 1. Настройка группы управления</span><span class="sxs-lookup"><span data-stu-id="c0302-111">Example 1: Configure a management group</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Update-AzApiManagementGateway -Context $apimContext -GatewayId "0001" -Description "Updated Gateway"
```

<span data-ttu-id="c0302-112">Эта команда настраивает шлюз.</span><span class="sxs-lookup"><span data-stu-id="c0302-112">This command configures a gateway.</span></span>

## <span data-ttu-id="c0302-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c0302-113">PARAMETERS</span></span>

### <span data-ttu-id="c0302-114">-Контекст</span><span class="sxs-lookup"><span data-stu-id="c0302-114">-Context</span></span>
<span data-ttu-id="c0302-115">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="c0302-115">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="c0302-116">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="c0302-116">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c0302-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0302-117">-DefaultProfile</span></span>
<span data-ttu-id="c0302-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c0302-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0302-119">-Description</span><span class="sxs-lookup"><span data-stu-id="c0302-119">-Description</span></span>
<span data-ttu-id="c0302-120">Описание шлюза.</span><span class="sxs-lookup"><span data-stu-id="c0302-120">Gateway description.</span></span>
<span data-ttu-id="c0302-121">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="c0302-121">This parameter is optional.</span></span>

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

### <span data-ttu-id="c0302-122">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="c0302-122">-GatewayId</span></span>
<span data-ttu-id="c0302-123">Идентификатор существующего шлюза.</span><span class="sxs-lookup"><span data-stu-id="c0302-123">Identifier of existing gateway.</span></span>
<span data-ttu-id="c0302-124">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="c0302-124">This parameter is required.</span></span>

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

### <span data-ttu-id="c0302-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c0302-125">-InputObject</span></span>
<span data-ttu-id="c0302-126">Экземпляр PsApiManagementGateway.</span><span class="sxs-lookup"><span data-stu-id="c0302-126">Instance of PsApiManagementGateway.</span></span> <span data-ttu-id="c0302-127">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="c0302-127">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c0302-128">-LocationData</span><span class="sxs-lookup"><span data-stu-id="c0302-128">-LocationData</span></span>
<span data-ttu-id="c0302-129">Расположение шлюза.</span><span class="sxs-lookup"><span data-stu-id="c0302-129">Gateway location.</span></span>
<span data-ttu-id="c0302-130">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="c0302-130">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResourceLocation
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0302-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c0302-131">-PassThru</span></span>
<span data-ttu-id="c0302-132">Если задан тип Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway, представляющий измененный шлюз.</span><span class="sxs-lookup"><span data-stu-id="c0302-132">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway type representing the modified gateway.</span></span>

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

### <span data-ttu-id="c0302-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c0302-133">-ResourceId</span></span>
<span data-ttu-id="c0302-134">Arm ResourceId шлюза.</span><span class="sxs-lookup"><span data-stu-id="c0302-134">Arm ResourceId of the Gateway.</span></span> <span data-ttu-id="c0302-135">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="c0302-135">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0302-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c0302-136">-Confirm</span></span>
<span data-ttu-id="c0302-137">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c0302-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0302-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0302-138">-WhatIf</span></span>
<span data-ttu-id="c0302-139">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c0302-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0302-140">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="c0302-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0302-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0302-141">CommonParameters</span></span>
<span data-ttu-id="c0302-142">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0302-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0302-143">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c0302-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0302-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c0302-144">INPUTS</span></span>

### <span data-ttu-id="c0302-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="c0302-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="c0302-146">System.String</span><span class="sxs-lookup"><span data-stu-id="c0302-146">System.String</span></span>

### <span data-ttu-id="c0302-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResourceLocation</span><span class="sxs-lookup"><span data-stu-id="c0302-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResourceLocation</span></span>

### <span data-ttu-id="c0302-148">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="c0302-148">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="c0302-149">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c0302-149">OUTPUTS</span></span>

### <span data-ttu-id="c0302-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="c0302-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway</span></span>

## <span data-ttu-id="c0302-151">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c0302-151">NOTES</span></span>

## <span data-ttu-id="c0302-152">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c0302-152">RELATED LINKS</span></span>
