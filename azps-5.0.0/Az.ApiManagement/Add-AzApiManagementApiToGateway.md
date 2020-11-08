---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/add-azapimanagementapitogateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementApiToGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementApiToGateway.md
ms.openlocfilehash: 6bb40d46c80e609824b1c56d05091ade5716f7f8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247892"
---
# <span data-ttu-id="fd141-101">Add-AzApiManagementApiToGateway</span><span class="sxs-lookup"><span data-stu-id="fd141-101">Add-AzApiManagementApiToGateway</span></span>

## <span data-ttu-id="fd141-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fd141-102">SYNOPSIS</span></span>
<span data-ttu-id="fd141-103">Подключает интерфейс API к шлюзу.</span><span class="sxs-lookup"><span data-stu-id="fd141-103">Attaches an API to a gateway.</span></span>

## <span data-ttu-id="fd141-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fd141-104">SYNTAX</span></span>

```
Add-AzApiManagementApiToGateway -Context <PsApiManagementContext> -GatewayId <String> -ApiId <String>
 [-ProvisioningState <PsApiManagementGatewayApiProvisioningState>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd141-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fd141-105">DESCRIPTION</span></span>
<span data-ttu-id="fd141-106">Командлет **Add-AzApiManagementApiToGateway** добавляет API управления Azure API на шлюз.</span><span class="sxs-lookup"><span data-stu-id="fd141-106">The **Add-AzApiManagementApiToGateway** cmdlet adds an Azure API Management API to a Gateway.</span></span>

## <span data-ttu-id="fd141-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fd141-107">EXAMPLES</span></span>

### <span data-ttu-id="fd141-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="fd141-108">Example 1</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Add-AzApiManagementApiToGateway -Context $ApiMgmtContext -GatewayId "0123456789" -ApiId "0001"
```

<span data-ttu-id="fd141-109">Эта команда добавляет указанный API к указанному шлюзу.</span><span class="sxs-lookup"><span data-stu-id="fd141-109">This command adds the specified API to the specified Gateway.</span></span>

## <span data-ttu-id="fd141-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fd141-110">PARAMETERS</span></span>

### <span data-ttu-id="fd141-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="fd141-111">-ApiId</span></span>
<span data-ttu-id="fd141-112">Идентификатор существующего API.</span><span class="sxs-lookup"><span data-stu-id="fd141-112">Identifier of existing API.</span></span>
<span data-ttu-id="fd141-113">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="fd141-113">This parameter is required.</span></span>

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

### <span data-ttu-id="fd141-114">-Context</span><span class="sxs-lookup"><span data-stu-id="fd141-114">-Context</span></span>
<span data-ttu-id="fd141-115">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="fd141-115">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="fd141-116">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="fd141-116">This parameter is required.</span></span>

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

### <span data-ttu-id="fd141-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd141-117">-DefaultProfile</span></span>
<span data-ttu-id="fd141-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fd141-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd141-119">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="fd141-119">-GatewayId</span></span>
<span data-ttu-id="fd141-120">Идентификатор существующего шлюза.</span><span class="sxs-lookup"><span data-stu-id="fd141-120">Identifier of existing gateway.</span></span>
<span data-ttu-id="fd141-121">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="fd141-121">This parameter is required.</span></span>

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

### <span data-ttu-id="fd141-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fd141-122">-PassThru</span></span>
<span data-ttu-id="fd141-123">Если задано значение true, операция Case запишется успешно.</span><span class="sxs-lookup"><span data-stu-id="fd141-123">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="fd141-124">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="fd141-124">This parameter is optional.</span></span>
<span data-ttu-id="fd141-125">Значение по умолчанию — false.</span><span class="sxs-lookup"><span data-stu-id="fd141-125">Default value is false.</span></span>

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

### <span data-ttu-id="fd141-126">-ProvisioningState</span><span class="sxs-lookup"><span data-stu-id="fd141-126">-ProvisioningState</span></span>
<span data-ttu-id="fd141-127">Состояние подготовки (создано).</span><span class="sxs-lookup"><span data-stu-id="fd141-127">Provisioning State (Created).</span></span>
<span data-ttu-id="fd141-128">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="fd141-128">This parameter is optional.</span></span>

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

### <span data-ttu-id="fd141-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fd141-129">-Confirm</span></span>
<span data-ttu-id="fd141-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="fd141-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd141-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd141-131">-WhatIf</span></span>
<span data-ttu-id="fd141-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="fd141-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fd141-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="fd141-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd141-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd141-134">CommonParameters</span></span>
<span data-ttu-id="fd141-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fd141-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd141-136">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fd141-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd141-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fd141-137">INPUTS</span></span>

### <span data-ttu-id="fd141-138">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="fd141-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="fd141-139">System. String</span><span class="sxs-lookup"><span data-stu-id="fd141-139">System.String</span></span>

### <span data-ttu-id="fd141-140">System. Nullable "1 [[Microsoft. Azure. Commands. ApiManagement. ServiceManagement.. PsApiManagementGatewayApiProvisioningState, Microsoft. Azure. PowerShell. командлеты. ApiManagement. ServiceManagement, Version = 2.0.1.0, культура = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="fd141-140">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayApiProvisioningState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=2.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="fd141-141">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="fd141-141">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="fd141-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fd141-142">OUTPUTS</span></span>

### <span data-ttu-id="fd141-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fd141-143">System.Boolean</span></span>

## <span data-ttu-id="fd141-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="fd141-144">NOTES</span></span>

## <span data-ttu-id="fd141-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fd141-145">RELATED LINKS</span></span>

[<span data-ttu-id="fd141-146">Remove-AzApiManagementApiFromGateway</span><span class="sxs-lookup"><span data-stu-id="fd141-146">Remove-AzApiManagementApiFromGateway</span></span>](./Remove-AzApiManagementApiFromGateway.md)