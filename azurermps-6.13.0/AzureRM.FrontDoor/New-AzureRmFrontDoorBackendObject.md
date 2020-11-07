---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/new-azurermfrontdoorbackendobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorBackendObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorBackendObject.md
ms.openlocfilehash: 429db1fae2987531911bd4dfbd4c41daf66a5440
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732933"
---
# <span data-ttu-id="05b96-101">New-AzureRmFrontDoorBackendObject</span><span class="sxs-lookup"><span data-stu-id="05b96-101">New-AzureRmFrontDoorBackendObject</span></span>

## <span data-ttu-id="05b96-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="05b96-102">SYNOPSIS</span></span>
<span data-ttu-id="05b96-103">Создание объекта PSBackend</span><span class="sxs-lookup"><span data-stu-id="05b96-103">Create a PSBackend object</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="05b96-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="05b96-104">SYNTAX</span></span>

```
New-AzureRmFrontDoorBackendObject -Address <String> [-HttpPort <Int32>] [-HttpsPort <Int32>]
 [-Priority <Int32>] [-Weight <Int32>] [-EnabledState <PSEnabledState>] [-BackendHostHeader <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="05b96-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="05b96-105">DESCRIPTION</span></span>
<span data-ttu-id="05b96-106">Создание объекта PSBackend для создания передней дверцы</span><span class="sxs-lookup"><span data-stu-id="05b96-106">Create a PSBackend object for Front Door creation</span></span>

## <span data-ttu-id="05b96-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="05b96-107">EXAMPLES</span></span>

### <span data-ttu-id="05b96-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="05b96-108">Example 1</span></span>
```powershell
PS C:\>New-AzureRmFrontDoorBackendObject -Address "contoso1.azurewebsites.net"


Address           : contoso1.azurewebsites.net
HttpPort          : 80
HttpsPort         : 443
Priority          : 1
Weight            : 50
BackendHostHeader :
EnabledState      : Enabled
```

<span data-ttu-id="05b96-109">Создание объекта PSBackend для создания передней дверцы</span><span class="sxs-lookup"><span data-stu-id="05b96-109">Create a PSBackend object for Front Door creation</span></span>

## <span data-ttu-id="05b96-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="05b96-110">PARAMETERS</span></span>

### <span data-ttu-id="05b96-111">-Address (адрес)</span><span class="sxs-lookup"><span data-stu-id="05b96-111">-Address</span></span>
<span data-ttu-id="05b96-112">Расположение внутреннего сервера (IP-адрес или полное доменное имя)</span><span class="sxs-lookup"><span data-stu-id="05b96-112">Location of the backend (IP address or FQDN)</span></span>

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

### <span data-ttu-id="05b96-113">-BackendHostHeader</span><span class="sxs-lookup"><span data-stu-id="05b96-113">-BackendHostHeader</span></span>
<span data-ttu-id="05b96-114">Значение, которое будет использоваться в качестве заголовка узла, отправляемого в сервер.</span><span class="sxs-lookup"><span data-stu-id="05b96-114">The value to use as the host header sent to the backend.</span></span> <span data-ttu-id="05b96-115">Значение по умолчанию — серверный адрес.</span><span class="sxs-lookup"><span data-stu-id="05b96-115">Default value is the backend address.</span></span>

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

### <span data-ttu-id="05b96-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05b96-116">-DefaultProfile</span></span>
<span data-ttu-id="05b96-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="05b96-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05b96-118">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="05b96-118">-EnabledState</span></span>
<span data-ttu-id="05b96-119">Следует ли включить использование этого внутреннего сервера.</span><span class="sxs-lookup"><span data-stu-id="05b96-119">Whether to enable use of this backend.</span></span> <span data-ttu-id="05b96-120">Значение по умолчанию — Enabled</span><span class="sxs-lookup"><span data-stu-id="05b96-120">Default value is Enabled</span></span>

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

### <span data-ttu-id="05b96-121">-HttpPort</span><span class="sxs-lookup"><span data-stu-id="05b96-121">-HttpPort</span></span>
<span data-ttu-id="05b96-122">Номер HTTP-порта TCP.</span><span class="sxs-lookup"><span data-stu-id="05b96-122">The HTTP TCP port number.</span></span>
<span data-ttu-id="05b96-123">Должно быть в диапазоне от 1 до 65535.</span><span class="sxs-lookup"><span data-stu-id="05b96-123">Must be between 1 and 65535.</span></span>
<span data-ttu-id="05b96-124">Значение по умолчанию — 80.</span><span class="sxs-lookup"><span data-stu-id="05b96-124">Default value is 80.</span></span>

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

### <span data-ttu-id="05b96-125">-HttpsPort</span><span class="sxs-lookup"><span data-stu-id="05b96-125">-HttpsPort</span></span>
<span data-ttu-id="05b96-126">Номер TCP порта HTTPS.</span><span class="sxs-lookup"><span data-stu-id="05b96-126">The HTTPS TCP port number.</span></span>
<span data-ttu-id="05b96-127">Должно быть в диапазоне от 1 до 65535.</span><span class="sxs-lookup"><span data-stu-id="05b96-127">Must be between 1 and 65535.</span></span>
<span data-ttu-id="05b96-128">Значение по умолчанию — 443</span><span class="sxs-lookup"><span data-stu-id="05b96-128">Default value is 443</span></span>

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

### <span data-ttu-id="05b96-129">-Priority (приоритет)</span><span class="sxs-lookup"><span data-stu-id="05b96-129">-Priority</span></span>
<span data-ttu-id="05b96-130">Приоритет, который необходимо использовать для балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="05b96-130">Priority to use for load balancing.</span></span>
<span data-ttu-id="05b96-131">Должно быть в диапазоне от 1 до 5.</span><span class="sxs-lookup"><span data-stu-id="05b96-131">Must be between 1 and 5.</span></span>
<span data-ttu-id="05b96-132">Значение по умолчанию — 1</span><span class="sxs-lookup"><span data-stu-id="05b96-132">Default value is 1</span></span>

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

### <span data-ttu-id="05b96-133">-Weight</span><span class="sxs-lookup"><span data-stu-id="05b96-133">-Weight</span></span>
<span data-ttu-id="05b96-134">Вес данной конечной точки в целях балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="05b96-134">Weight of this endpoint for load balancing purposes.</span></span>
<span data-ttu-id="05b96-135">Должно быть в диапазоне от 1 до 1000.</span><span class="sxs-lookup"><span data-stu-id="05b96-135">Must be between 1 and 1000.</span></span>
<span data-ttu-id="05b96-136">Значение по умолчанию — 50</span><span class="sxs-lookup"><span data-stu-id="05b96-136">Default value is 50</span></span>

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

### <span data-ttu-id="05b96-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05b96-137">CommonParameters</span></span>
<span data-ttu-id="05b96-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="05b96-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05b96-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05b96-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05b96-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="05b96-140">INPUTS</span></span>

### <span data-ttu-id="05b96-141">Ничего</span><span class="sxs-lookup"><span data-stu-id="05b96-141">None</span></span>

## <span data-ttu-id="05b96-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="05b96-142">OUTPUTS</span></span>

### <span data-ttu-id="05b96-143">Microsoft. Azure. Commands. FrontDoor. Models. PSBackend</span><span class="sxs-lookup"><span data-stu-id="05b96-143">Microsoft.Azure.Commands.FrontDoor.Models.PSBackend</span></span>

## <span data-ttu-id="05b96-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="05b96-144">NOTES</span></span>

## <span data-ttu-id="05b96-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="05b96-145">RELATED LINKS</span></span>

[<span data-ttu-id="05b96-146">New-AzureRmFrontDoorBackendPoolObject</span><span class="sxs-lookup"><span data-stu-id="05b96-146">New-AzureRmFrontDoorBackendPoolObject</span></span>](./New-AzureRmFrontDoorBackendPoolObject.md)
