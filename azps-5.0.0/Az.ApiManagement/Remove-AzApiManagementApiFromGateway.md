---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapifromgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiFromGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiFromGateway.md
ms.openlocfilehash: 506287812f684a778fdb96e750aac34049912b58
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249727"
---
# <span data-ttu-id="25fde-101">Remove-AzApiManagementApiFromGateway</span><span class="sxs-lookup"><span data-stu-id="25fde-101">Remove-AzApiManagementApiFromGateway</span></span>

## <span data-ttu-id="25fde-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="25fde-102">SYNOPSIS</span></span>
<span data-ttu-id="25fde-103">Подключает интерфейс API к шлюзу.</span><span class="sxs-lookup"><span data-stu-id="25fde-103">Attaches an API to a gateway.</span></span>

## <span data-ttu-id="25fde-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="25fde-104">SYNTAX</span></span>

```
Remove-AzApiManagementApiFromGateway -Context <PsApiManagementContext> -GatewayId <String> -ApiId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="25fde-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="25fde-105">DESCRIPTION</span></span>
<span data-ttu-id="25fde-106">Командлет **Remove-AzApiManagementApiFromGateway** прикрепляет интерфейс API к шлюзу.</span><span class="sxs-lookup"><span data-stu-id="25fde-106">The **Remove-AzApiManagementApiFromGateway** cmdlet attaches an API to a gateway.</span></span>

## <span data-ttu-id="25fde-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="25fde-107">EXAMPLES</span></span>

### <span data-ttu-id="25fde-108">Пример 1: удаление API-интерфейса из шлюза</span><span class="sxs-lookup"><span data-stu-id="25fde-108">Example 1: Remove an API from a gateway</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementApiFromGateway -Context $ApiMgmtContext -GatewayId "0123456789" -ApiId "0001" -PassThru
```

<span data-ttu-id="25fde-109">Эта команда удаляет указанный API из шлюза.</span><span class="sxs-lookup"><span data-stu-id="25fde-109">This command removes the specified API from a gateway.</span></span>

## <span data-ttu-id="25fde-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="25fde-110">PARAMETERS</span></span>

### <span data-ttu-id="25fde-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="25fde-111">-ApiId</span></span>
<span data-ttu-id="25fde-112">Идентификатор существующих API-интерфейсов, которые нужно удалить из шлюза.</span><span class="sxs-lookup"><span data-stu-id="25fde-112">Identifier of existing APIs to remove from the Gateway.</span></span>
<span data-ttu-id="25fde-113">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="25fde-113">This parameter is required.</span></span>

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

### <span data-ttu-id="25fde-114">-Context</span><span class="sxs-lookup"><span data-stu-id="25fde-114">-Context</span></span>
<span data-ttu-id="25fde-115">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="25fde-115">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="25fde-116">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="25fde-116">This parameter is required.</span></span>

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

### <span data-ttu-id="25fde-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25fde-117">-DefaultProfile</span></span>
<span data-ttu-id="25fde-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="25fde-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="25fde-119">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="25fde-119">-GatewayId</span></span>
<span data-ttu-id="25fde-120">Идентификатор существующего шлюза, из которого нужно удалить API.</span><span class="sxs-lookup"><span data-stu-id="25fde-120">Identifier of existing Gateway to remove API from.</span></span>
<span data-ttu-id="25fde-121">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="25fde-121">This parameter is required.</span></span>

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

### <span data-ttu-id="25fde-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="25fde-122">-PassThru</span></span>
<span data-ttu-id="25fde-123">Если задано значение true, операция Case запишется успешно.</span><span class="sxs-lookup"><span data-stu-id="25fde-123">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="25fde-124">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="25fde-124">This parameter is optional.</span></span>
<span data-ttu-id="25fde-125">Значение по умолчанию — false.</span><span class="sxs-lookup"><span data-stu-id="25fde-125">Default value is false.</span></span>

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

### <span data-ttu-id="25fde-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="25fde-126">-Confirm</span></span>
<span data-ttu-id="25fde-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="25fde-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25fde-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25fde-128">-WhatIf</span></span>
<span data-ttu-id="25fde-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="25fde-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="25fde-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="25fde-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25fde-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25fde-131">CommonParameters</span></span>
<span data-ttu-id="25fde-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="25fde-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25fde-133">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="25fde-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25fde-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="25fde-134">INPUTS</span></span>

### <span data-ttu-id="25fde-135">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="25fde-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="25fde-136">System. String</span><span class="sxs-lookup"><span data-stu-id="25fde-136">System.String</span></span>

### <span data-ttu-id="25fde-137">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="25fde-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="25fde-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="25fde-138">OUTPUTS</span></span>

### <span data-ttu-id="25fde-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="25fde-139">System.Boolean</span></span>

## <span data-ttu-id="25fde-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="25fde-140">NOTES</span></span>

## <span data-ttu-id="25fde-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="25fde-141">RELATED LINKS</span></span>
