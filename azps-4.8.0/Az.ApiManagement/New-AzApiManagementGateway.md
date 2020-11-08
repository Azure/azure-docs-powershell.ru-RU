---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementGateway.md
ms.openlocfilehash: c06442ef9ab4b5f80943da33ed87fc24c276107d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235146"
---
# <span data-ttu-id="c6298-101">New-AzApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="c6298-101">New-AzApiManagementGateway</span></span>

## <span data-ttu-id="c6298-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c6298-102">SYNOPSIS</span></span>
<span data-ttu-id="c6298-103">Создает новую сущность Gateway.</span><span class="sxs-lookup"><span data-stu-id="c6298-103">Creates new Gateway entity.</span></span>

## <span data-ttu-id="c6298-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c6298-104">SYNTAX</span></span>

```
New-AzApiManagementGateway -Context <PsApiManagementContext> [-GatewayId <String>] [-Description <String>]
 -LocationData <PsApiManagementResourceLocation> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c6298-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c6298-105">DESCRIPTION</span></span>
<span data-ttu-id="c6298-106">Командлет **New-AzApiManagementGateway** создает новую сущность Gateway.</span><span class="sxs-lookup"><span data-stu-id="c6298-106">The **New-AzApiManagementGateway** cmdlet creates new Gateway entity.</span></span>

## <span data-ttu-id="c6298-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c6298-107">EXAMPLES</span></span>

### <span data-ttu-id="c6298-108">Пример 1: Создание шлюза</span><span class="sxs-lookup"><span data-stu-id="c6298-108">Example 1: Create a gateway</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$location = New-AzApiManagementResourceLocationObject -Name "n1" -City "c1" -District "d1" -CountryOrRegion "r1"
PS C:\>New-AzApiManagementGateway -Context $apimContext -GatewayId "123" -Description "desc" -LocationData $location
```

<span data-ttu-id="c6298-109">Эта команда создает шлюз.</span><span class="sxs-lookup"><span data-stu-id="c6298-109">This command creates a gateway.</span></span>

## <span data-ttu-id="c6298-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c6298-110">PARAMETERS</span></span>

### <span data-ttu-id="c6298-111">-Context</span><span class="sxs-lookup"><span data-stu-id="c6298-111">-Context</span></span>
<span data-ttu-id="c6298-112">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="c6298-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="c6298-113">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="c6298-113">This parameter is required.</span></span>

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

### <span data-ttu-id="c6298-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6298-114">-DefaultProfile</span></span>
<span data-ttu-id="c6298-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c6298-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c6298-116">-Описание</span><span class="sxs-lookup"><span data-stu-id="c6298-116">-Description</span></span>
<span data-ttu-id="c6298-117">Описание шлюза.</span><span class="sxs-lookup"><span data-stu-id="c6298-117">Gateway description.</span></span>
<span data-ttu-id="c6298-118">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="c6298-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="c6298-119">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="c6298-119">-GatewayId</span></span>
<span data-ttu-id="c6298-120">Идентификатор нового шлюза.</span><span class="sxs-lookup"><span data-stu-id="c6298-120">Identifier of new gateway.</span></span>
<span data-ttu-id="c6298-121">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="c6298-121">This parameter is optional.</span></span>
<span data-ttu-id="c6298-122">Если не указано, будет создано.</span><span class="sxs-lookup"><span data-stu-id="c6298-122">If not specified will be generated.</span></span>

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

### <span data-ttu-id="c6298-123">-LocationData</span><span class="sxs-lookup"><span data-stu-id="c6298-123">-LocationData</span></span>
<span data-ttu-id="c6298-124">Расположение шлюза.</span><span class="sxs-lookup"><span data-stu-id="c6298-124">Gateway location.</span></span>
<span data-ttu-id="c6298-125">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="c6298-125">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResourceLocation
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6298-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c6298-126">-Confirm</span></span>
<span data-ttu-id="c6298-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c6298-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6298-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6298-128">-WhatIf</span></span>
<span data-ttu-id="c6298-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c6298-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c6298-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c6298-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c6298-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6298-131">CommonParameters</span></span>
<span data-ttu-id="c6298-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c6298-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6298-133">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c6298-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6298-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c6298-134">INPUTS</span></span>

### <span data-ttu-id="c6298-135">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="c6298-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="c6298-136">System. String</span><span class="sxs-lookup"><span data-stu-id="c6298-136">System.String</span></span>

### <span data-ttu-id="c6298-137">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementResourceLocation</span><span class="sxs-lookup"><span data-stu-id="c6298-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResourceLocation</span></span>

## <span data-ttu-id="c6298-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c6298-138">OUTPUTS</span></span>

### <span data-ttu-id="c6298-139">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="c6298-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway</span></span>

## <span data-ttu-id="c6298-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="c6298-140">NOTES</span></span>

## <span data-ttu-id="c6298-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c6298-141">RELATED LINKS</span></span>