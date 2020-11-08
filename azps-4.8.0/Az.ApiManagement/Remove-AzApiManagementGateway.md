---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementGateway.md
ms.openlocfilehash: 9b6eac7a0c0c994797de51c936840da515ef3f4c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078550"
---
# <span data-ttu-id="40b12-101">Remove-AzApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="40b12-101">Remove-AzApiManagementGateway</span></span>

## <span data-ttu-id="40b12-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="40b12-102">SYNOPSIS</span></span>
<span data-ttu-id="40b12-103">Отсоединяет API-интерфейс от шлюза.</span><span class="sxs-lookup"><span data-stu-id="40b12-103">Detaches an API from a Gateway.</span></span>

## <span data-ttu-id="40b12-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="40b12-104">SYNTAX</span></span>

### <span data-ttu-id="40b12-105">ContextParameterSetName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="40b12-105">ContextParameterSetName (Default)</span></span>
```
Remove-AzApiManagementGateway -Context <PsApiManagementContext> -GatewayId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="40b12-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="40b12-106">ByInputObjectParameterSet</span></span>
```
Remove-AzApiManagementGateway -InputObject <PsApiManagementGateway> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="40b12-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="40b12-107">ByResourceIdParameterSet</span></span>
```
Remove-AzApiManagementGateway -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="40b12-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="40b12-108">DESCRIPTION</span></span>
<span data-ttu-id="40b12-109">Командлет **Remove-AzApiManagementGateway** отключает API-интерфейс от шлюза.</span><span class="sxs-lookup"><span data-stu-id="40b12-109">The **Remove-AzApiManagementGateway** cmdlet detaches an API from a Gateway.</span></span>

## <span data-ttu-id="40b12-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="40b12-110">EXAMPLES</span></span>

### <span data-ttu-id="40b12-111">Пример 1: удаление существующего шлюза</span><span class="sxs-lookup"><span data-stu-id="40b12-111">Example 1: Remove an existing gateway</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementGateway -Context $apimContext -GatewayId "g0001" -Force
```

<span data-ttu-id="40b12-112">Эта команда удаляет существующий шлюз и не запрашивает подтверждение у пользователя.</span><span class="sxs-lookup"><span data-stu-id="40b12-112">This command removes an existing gateway and does not prompt the user for confirmation.</span></span>

## <span data-ttu-id="40b12-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="40b12-113">PARAMETERS</span></span>

### <span data-ttu-id="40b12-114">-Context</span><span class="sxs-lookup"><span data-stu-id="40b12-114">-Context</span></span>
<span data-ttu-id="40b12-115">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="40b12-115">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="40b12-116">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="40b12-116">This parameter is required.</span></span>

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

### <span data-ttu-id="40b12-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40b12-117">-DefaultProfile</span></span>
<span data-ttu-id="40b12-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="40b12-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40b12-119">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="40b12-119">-GatewayId</span></span>
<span data-ttu-id="40b12-120">Идентификатор существующего шлюза.</span><span class="sxs-lookup"><span data-stu-id="40b12-120">Identifier of existing gateway.</span></span>
<span data-ttu-id="40b12-121">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="40b12-121">This parameter is required.</span></span>

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

### <span data-ttu-id="40b12-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="40b12-122">-InputObject</span></span>
<span data-ttu-id="40b12-123">Экземпляр PsApiManagementGateway.</span><span class="sxs-lookup"><span data-stu-id="40b12-123">Instance of PsApiManagementGateway.</span></span> <span data-ttu-id="40b12-124">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="40b12-124">This parameter is required.</span></span>

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

### <span data-ttu-id="40b12-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="40b12-125">-PassThru</span></span>
<span data-ttu-id="40b12-126">Если задано значение true, операция Case запишется успешно.</span><span class="sxs-lookup"><span data-stu-id="40b12-126">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="40b12-127">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="40b12-127">This parameter is optional.</span></span>
<span data-ttu-id="40b12-128">Значение по умолчанию — false.</span><span class="sxs-lookup"><span data-stu-id="40b12-128">Default value is false.</span></span>

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

### <span data-ttu-id="40b12-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="40b12-129">-ResourceId</span></span>
<span data-ttu-id="40b12-130">ИД ресурса ARM для шлюза.</span><span class="sxs-lookup"><span data-stu-id="40b12-130">Arm ResourceId of the Gateway.</span></span> <span data-ttu-id="40b12-131">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="40b12-131">This parameter is required.</span></span>

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

### <span data-ttu-id="40b12-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="40b12-132">-Confirm</span></span>
<span data-ttu-id="40b12-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="40b12-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40b12-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40b12-134">-WhatIf</span></span>
<span data-ttu-id="40b12-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="40b12-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40b12-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="40b12-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40b12-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40b12-137">CommonParameters</span></span>
<span data-ttu-id="40b12-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="40b12-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40b12-139">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="40b12-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40b12-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="40b12-140">INPUTS</span></span>

### <span data-ttu-id="40b12-141">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="40b12-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="40b12-142">System. String</span><span class="sxs-lookup"><span data-stu-id="40b12-142">System.String</span></span>

### <span data-ttu-id="40b12-143">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="40b12-143">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="40b12-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="40b12-144">OUTPUTS</span></span>

### <span data-ttu-id="40b12-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="40b12-145">System.Boolean</span></span>

## <span data-ttu-id="40b12-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="40b12-146">NOTES</span></span>

## <span data-ttu-id="40b12-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="40b12-147">RELATED LINKS</span></span>
