---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagementapifromgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiFromGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiFromGateway.md
ms.openlocfilehash: 2b50ddb0186e1c7ca8bc0da237f3fca833cb7367
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101959075"
---
# <span data-ttu-id="3fb9f-101">Remove-AzApiManagementApiFromGateway</span><span class="sxs-lookup"><span data-stu-id="3fb9f-101">Remove-AzApiManagementApiFromGateway</span></span>

## <span data-ttu-id="3fb9f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3fb9f-102">SYNOPSIS</span></span>
<span data-ttu-id="3fb9f-103">Прикрепит API к шлюзу.</span><span class="sxs-lookup"><span data-stu-id="3fb9f-103">Attaches an API to a gateway.</span></span>

## <span data-ttu-id="3fb9f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="3fb9f-104">SYNTAX</span></span>

```
Remove-AzApiManagementApiFromGateway -Context <PsApiManagementContext> -GatewayId <String> -ApiId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3fb9f-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3fb9f-105">DESCRIPTION</span></span>
<span data-ttu-id="3fb9f-106">**Cmdlet Remove-AzApiManagementApiFromGateway** прикрепит API к шлюзу.</span><span class="sxs-lookup"><span data-stu-id="3fb9f-106">The **Remove-AzApiManagementApiFromGateway** cmdlet attaches an API to a gateway.</span></span>

## <span data-ttu-id="3fb9f-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="3fb9f-107">EXAMPLES</span></span>

### <span data-ttu-id="3fb9f-108">Пример 1. Удаление API из шлюза</span><span class="sxs-lookup"><span data-stu-id="3fb9f-108">Example 1: Remove an API from a gateway</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementApiFromGateway -Context $ApiMgmtContext -GatewayId "0123456789" -ApiId "0001" -PassThru
```

<span data-ttu-id="3fb9f-109">Эта команда удаляет указанный API из шлюза.</span><span class="sxs-lookup"><span data-stu-id="3fb9f-109">This command removes the specified API from a gateway.</span></span>

## <span data-ttu-id="3fb9f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3fb9f-110">PARAMETERS</span></span>

### <span data-ttu-id="3fb9f-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="3fb9f-111">-ApiId</span></span>
<span data-ttu-id="3fb9f-112">Идентификатор существующих API, которые нужно удалить из шлюза.</span><span class="sxs-lookup"><span data-stu-id="3fb9f-112">Identifier of existing APIs to remove from the Gateway.</span></span>
<span data-ttu-id="3fb9f-113">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="3fb9f-113">This parameter is required.</span></span>

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

### <span data-ttu-id="3fb9f-114">-Контекст</span><span class="sxs-lookup"><span data-stu-id="3fb9f-114">-Context</span></span>
<span data-ttu-id="3fb9f-115">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="3fb9f-115">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="3fb9f-116">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="3fb9f-116">This parameter is required.</span></span>

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

### <span data-ttu-id="3fb9f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3fb9f-117">-DefaultProfile</span></span>
<span data-ttu-id="3fb9f-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3fb9f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3fb9f-119">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="3fb9f-119">-GatewayId</span></span>
<span data-ttu-id="3fb9f-120">Идентификатор существующего шлюза для удаления API.</span><span class="sxs-lookup"><span data-stu-id="3fb9f-120">Identifier of existing Gateway to remove API from.</span></span>
<span data-ttu-id="3fb9f-121">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="3fb9f-121">This parameter is required.</span></span>

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

### <span data-ttu-id="3fb9f-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3fb9f-122">-PassThru</span></span>
<span data-ttu-id="3fb9f-123">Если этот задан, будет указано "Истина" в случае успешной операции.</span><span class="sxs-lookup"><span data-stu-id="3fb9f-123">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="3fb9f-124">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="3fb9f-124">This parameter is optional.</span></span>
<span data-ttu-id="3fb9f-125">Значение по умолчанию — false.</span><span class="sxs-lookup"><span data-stu-id="3fb9f-125">Default value is false.</span></span>

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

### <span data-ttu-id="3fb9f-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3fb9f-126">-Confirm</span></span>
<span data-ttu-id="3fb9f-127">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="3fb9f-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3fb9f-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3fb9f-128">-WhatIf</span></span>
<span data-ttu-id="3fb9f-129">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3fb9f-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3fb9f-130">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="3fb9f-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3fb9f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fb9f-131">CommonParameters</span></span>
<span data-ttu-id="3fb9f-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3fb9f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fb9f-133">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3fb9f-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fb9f-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3fb9f-134">INPUTS</span></span>

### <span data-ttu-id="3fb9f-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="3fb9f-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="3fb9f-136">System.String</span><span class="sxs-lookup"><span data-stu-id="3fb9f-136">System.String</span></span>

### <span data-ttu-id="3fb9f-137">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="3fb9f-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="3fb9f-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3fb9f-138">OUTPUTS</span></span>

### <span data-ttu-id="3fb9f-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3fb9f-139">System.Boolean</span></span>

## <span data-ttu-id="3fb9f-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="3fb9f-140">NOTES</span></span>

## <span data-ttu-id="3fb9f-141">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3fb9f-141">RELATED LINKS</span></span>
