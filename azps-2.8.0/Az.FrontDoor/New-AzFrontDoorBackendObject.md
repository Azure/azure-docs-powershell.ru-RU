---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorbackendobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendObject.md
ms.openlocfilehash: 5cf730c5ba450978730617b7ddb270c0fdec2bf9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720897"
---
# <span data-ttu-id="ae7ac-101">New-AzFrontDoorBackendObject</span><span class="sxs-lookup"><span data-stu-id="ae7ac-101">New-AzFrontDoorBackendObject</span></span>

## <span data-ttu-id="ae7ac-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ae7ac-102">SYNOPSIS</span></span>
<span data-ttu-id="ae7ac-103">Создание объекта PSBackend</span><span class="sxs-lookup"><span data-stu-id="ae7ac-103">Create a PSBackend object</span></span>

## <span data-ttu-id="ae7ac-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ae7ac-104">SYNTAX</span></span>

```
New-AzFrontDoorBackendObject -Address <String> [-HttpPort <Int32>] [-HttpsPort <Int32>] [-Priority <Int32>]
 [-Weight <Int32>] [-EnabledState <PSEnabledState>] [-BackendHostHeader <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ae7ac-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ae7ac-105">DESCRIPTION</span></span>
<span data-ttu-id="ae7ac-106">Создание объекта PSBackend для создания передней дверцы</span><span class="sxs-lookup"><span data-stu-id="ae7ac-106">Create a PSBackend object for Front Door creation</span></span>

## <span data-ttu-id="ae7ac-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ae7ac-107">EXAMPLES</span></span>

### <span data-ttu-id="ae7ac-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ae7ac-108">Example 1</span></span>
```powershell
PS C:\>New-AzFrontDoorBackendObject -Address "contoso1.azurewebsites.net"


Address           : contoso1.azurewebsites.net
HttpPort          : 80
HttpsPort         : 443
Priority          : 1
Weight            : 50
BackendHostHeader :
EnabledState      : Enabled
```

<span data-ttu-id="ae7ac-109">Создание объекта PSBackend для создания передней дверцы</span><span class="sxs-lookup"><span data-stu-id="ae7ac-109">Create a PSBackend object for Front Door creation</span></span>

## <span data-ttu-id="ae7ac-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ae7ac-110">PARAMETERS</span></span>

### <span data-ttu-id="ae7ac-111">-Address (адрес)</span><span class="sxs-lookup"><span data-stu-id="ae7ac-111">-Address</span></span>
<span data-ttu-id="ae7ac-112">Расположение внутреннего сервера (IP-адрес или полное доменное имя)</span><span class="sxs-lookup"><span data-stu-id="ae7ac-112">Location of the backend (IP address or FQDN)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae7ac-113">-BackendHostHeader</span><span class="sxs-lookup"><span data-stu-id="ae7ac-113">-BackendHostHeader</span></span>
<span data-ttu-id="ae7ac-114">Значение, которое будет использоваться в качестве заголовка узла, отправляемого в сервер.</span><span class="sxs-lookup"><span data-stu-id="ae7ac-114">The value to use as the host header sent to the backend.</span></span> <span data-ttu-id="ae7ac-115">Значение по умолчанию — серверный адрес.</span><span class="sxs-lookup"><span data-stu-id="ae7ac-115">Default value is the backend address.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae7ac-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae7ac-116">-DefaultProfile</span></span>
<span data-ttu-id="ae7ac-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ae7ac-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ae7ac-118">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="ae7ac-118">-EnabledState</span></span>
<span data-ttu-id="ae7ac-119">Следует ли включить использование этого внутреннего сервера.</span><span class="sxs-lookup"><span data-stu-id="ae7ac-119">Whether to enable use of this backend.</span></span> <span data-ttu-id="ae7ac-120">Значение по умолчанию — Enabled</span><span class="sxs-lookup"><span data-stu-id="ae7ac-120">Default value is Enabled</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSEnabledState
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae7ac-121">-HttpPort</span><span class="sxs-lookup"><span data-stu-id="ae7ac-121">-HttpPort</span></span>
<span data-ttu-id="ae7ac-122">Номер HTTP-порта TCP.</span><span class="sxs-lookup"><span data-stu-id="ae7ac-122">The HTTP TCP port number.</span></span>
<span data-ttu-id="ae7ac-123">Должно быть в диапазоне от 1 до 65535.</span><span class="sxs-lookup"><span data-stu-id="ae7ac-123">Must be between 1 and 65535.</span></span>
<span data-ttu-id="ae7ac-124">Значение по умолчанию — 80.</span><span class="sxs-lookup"><span data-stu-id="ae7ac-124">Default value is 80.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae7ac-125">-HttpsPort</span><span class="sxs-lookup"><span data-stu-id="ae7ac-125">-HttpsPort</span></span>
<span data-ttu-id="ae7ac-126">Номер TCP порта HTTPS.</span><span class="sxs-lookup"><span data-stu-id="ae7ac-126">The HTTPS TCP port number.</span></span>
<span data-ttu-id="ae7ac-127">Должно быть в диапазоне от 1 до 65535.</span><span class="sxs-lookup"><span data-stu-id="ae7ac-127">Must be between 1 and 65535.</span></span>
<span data-ttu-id="ae7ac-128">Значение по умолчанию — 443</span><span class="sxs-lookup"><span data-stu-id="ae7ac-128">Default value is 443</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae7ac-129">-Priority (приоритет)</span><span class="sxs-lookup"><span data-stu-id="ae7ac-129">-Priority</span></span>
<span data-ttu-id="ae7ac-130">Приоритет, который необходимо использовать для балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="ae7ac-130">Priority to use for load balancing.</span></span>
<span data-ttu-id="ae7ac-131">Должно быть в диапазоне от 1 до 5.</span><span class="sxs-lookup"><span data-stu-id="ae7ac-131">Must be between 1 and 5.</span></span>
<span data-ttu-id="ae7ac-132">Значение по умолчанию — 1</span><span class="sxs-lookup"><span data-stu-id="ae7ac-132">Default value is 1</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae7ac-133">-Weight</span><span class="sxs-lookup"><span data-stu-id="ae7ac-133">-Weight</span></span>
<span data-ttu-id="ae7ac-134">Вес данной конечной точки в целях балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="ae7ac-134">Weight of this endpoint for load balancing purposes.</span></span>
<span data-ttu-id="ae7ac-135">Должно быть в диапазоне от 1 до 1000.</span><span class="sxs-lookup"><span data-stu-id="ae7ac-135">Must be between 1 and 1000.</span></span>
<span data-ttu-id="ae7ac-136">Значение по умолчанию — 50</span><span class="sxs-lookup"><span data-stu-id="ae7ac-136">Default value is 50</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae7ac-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae7ac-137">CommonParameters</span></span>
<span data-ttu-id="ae7ac-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ae7ac-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae7ac-139">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ae7ac-139">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae7ac-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ae7ac-140">INPUTS</span></span>

### <span data-ttu-id="ae7ac-141">Ничего</span><span class="sxs-lookup"><span data-stu-id="ae7ac-141">None</span></span>

## <span data-ttu-id="ae7ac-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ae7ac-142">OUTPUTS</span></span>

### <span data-ttu-id="ae7ac-143">Microsoft. Azure. Commands. FrontDoor. Models. PSBackend</span><span class="sxs-lookup"><span data-stu-id="ae7ac-143">Microsoft.Azure.Commands.FrontDoor.Models.PSBackend</span></span>

## <span data-ttu-id="ae7ac-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="ae7ac-144">NOTES</span></span>

## <span data-ttu-id="ae7ac-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ae7ac-145">RELATED LINKS</span></span>

[<span data-ttu-id="ae7ac-146">New-AzFrontDoorBackendPoolObject</span><span class="sxs-lookup"><span data-stu-id="ae7ac-146">New-AzFrontDoorBackendPoolObject</span></span>](./New-AzFrontDoorBackendPoolObject.md)
