---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorbackendobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendObject.md
ms.openlocfilehash: 8eee112840fa7d7af81838927017b38988c9649b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247430"
---
# <span data-ttu-id="36518-101">New-AzFrontDoorBackendObject</span><span class="sxs-lookup"><span data-stu-id="36518-101">New-AzFrontDoorBackendObject</span></span>

## <span data-ttu-id="36518-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="36518-102">SYNOPSIS</span></span>
<span data-ttu-id="36518-103">Создание объекта PSBackend</span><span class="sxs-lookup"><span data-stu-id="36518-103">Create a PSBackend object</span></span>

## <span data-ttu-id="36518-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="36518-104">SYNTAX</span></span>

```
New-AzFrontDoorBackendObject -Address <String> [-HttpPort <Int32>] [-HttpsPort <Int32>] [-Priority <Int32>]
 [-Weight <Int32>] [-EnabledState <PSEnabledState>] [-BackendHostHeader <String>] [-PrivateLinkAlias <String>]
 [-PrivateLinkResourceId <String>] [-PrivateLinkLocation <String>] [-PrivateLinkApprovalMessage <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="36518-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="36518-105">DESCRIPTION</span></span>
<span data-ttu-id="36518-106">Создание объекта PSBackend для создания передней дверцы</span><span class="sxs-lookup"><span data-stu-id="36518-106">Create a PSBackend object for Front Door creation</span></span>

## <span data-ttu-id="36518-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="36518-107">EXAMPLES</span></span>

### <span data-ttu-id="36518-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="36518-108">Example 1</span></span>
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

<span data-ttu-id="36518-109">Создание объекта PSBackend для создания передней дверцы</span><span class="sxs-lookup"><span data-stu-id="36518-109">Create a PSBackend object for Front Door creation</span></span>

## <span data-ttu-id="36518-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="36518-110">PARAMETERS</span></span>

### <span data-ttu-id="36518-111">-Address (адрес)</span><span class="sxs-lookup"><span data-stu-id="36518-111">-Address</span></span>
<span data-ttu-id="36518-112">Расположение внутреннего сервера (IP-адрес или полное доменное имя)</span><span class="sxs-lookup"><span data-stu-id="36518-112">Location of the backend (IP address or FQDN)</span></span>

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

### <span data-ttu-id="36518-113">-BackendHostHeader</span><span class="sxs-lookup"><span data-stu-id="36518-113">-BackendHostHeader</span></span>
<span data-ttu-id="36518-114">Значение, которое будет использоваться в качестве заголовка узла, отправляемого в сервер.</span><span class="sxs-lookup"><span data-stu-id="36518-114">The value to use as the host header sent to the backend.</span></span> <span data-ttu-id="36518-115">Значение по умолчанию — серверный адрес.</span><span class="sxs-lookup"><span data-stu-id="36518-115">Default value is the backend address.</span></span>

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

### <span data-ttu-id="36518-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36518-116">-DefaultProfile</span></span>
<span data-ttu-id="36518-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="36518-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36518-118">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="36518-118">-EnabledState</span></span>
<span data-ttu-id="36518-119">Следует ли включить использование этого внутреннего сервера.</span><span class="sxs-lookup"><span data-stu-id="36518-119">Whether to enable use of this backend.</span></span> <span data-ttu-id="36518-120">Значение по умолчанию — Enabled</span><span class="sxs-lookup"><span data-stu-id="36518-120">Default value is Enabled</span></span>

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

### <span data-ttu-id="36518-121">-HttpPort</span><span class="sxs-lookup"><span data-stu-id="36518-121">-HttpPort</span></span>
<span data-ttu-id="36518-122">Номер HTTP-порта TCP.</span><span class="sxs-lookup"><span data-stu-id="36518-122">The HTTP TCP port number.</span></span>
<span data-ttu-id="36518-123">Должно быть в диапазоне от 1 до 65535.</span><span class="sxs-lookup"><span data-stu-id="36518-123">Must be between 1 and 65535.</span></span>
<span data-ttu-id="36518-124">Значение по умолчанию — 80.</span><span class="sxs-lookup"><span data-stu-id="36518-124">Default value is 80.</span></span>

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

### <span data-ttu-id="36518-125">-HttpsPort</span><span class="sxs-lookup"><span data-stu-id="36518-125">-HttpsPort</span></span>
<span data-ttu-id="36518-126">Номер TCP порта HTTPS.</span><span class="sxs-lookup"><span data-stu-id="36518-126">The HTTPS TCP port number.</span></span>
<span data-ttu-id="36518-127">Должно быть в диапазоне от 1 до 65535.</span><span class="sxs-lookup"><span data-stu-id="36518-127">Must be between 1 and 65535.</span></span>
<span data-ttu-id="36518-128">Значение по умолчанию — 443</span><span class="sxs-lookup"><span data-stu-id="36518-128">Default value is 443</span></span>

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

### <span data-ttu-id="36518-129">-Priority (приоритет)</span><span class="sxs-lookup"><span data-stu-id="36518-129">-Priority</span></span>
<span data-ttu-id="36518-130">Приоритет, который необходимо использовать для балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="36518-130">Priority to use for load balancing.</span></span>
<span data-ttu-id="36518-131">Должно быть в диапазоне от 1 до 5.</span><span class="sxs-lookup"><span data-stu-id="36518-131">Must be between 1 and 5.</span></span>
<span data-ttu-id="36518-132">Значение по умолчанию — 1</span><span class="sxs-lookup"><span data-stu-id="36518-132">Default value is 1</span></span>

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

### <span data-ttu-id="36518-133">-PrivateLinkAlias</span><span class="sxs-lookup"><span data-stu-id="36518-133">-PrivateLinkAlias</span></span>
<span data-ttu-id="36518-134">Псевдоним ресурса частной ссылки.</span><span class="sxs-lookup"><span data-stu-id="36518-134">The Alias of the Private Link resource.</span></span> <span data-ttu-id="36518-135">Заполнение этого необязательного поля указывает на то, что этот внутренний сервер является "Private"</span><span class="sxs-lookup"><span data-stu-id="36518-135">Populating this optional field indicates that this backend is 'Private'</span></span>

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

### <span data-ttu-id="36518-136">-PrivateLinkApprovalMessage</span><span class="sxs-lookup"><span data-stu-id="36518-136">-PrivateLinkApprovalMessage</span></span>
<span data-ttu-id="36518-137">Настраиваемое сообщение, которое должно быть включено в запрос на утверждение для подключения к частной ссылке</span><span class="sxs-lookup"><span data-stu-id="36518-137">A custom message to be included in the approval request to connect to the Private Link</span></span>

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

### <span data-ttu-id="36518-138">-PrivateLinkLocation</span><span class="sxs-lookup"><span data-stu-id="36518-138">-PrivateLinkLocation</span></span>
<span data-ttu-id="36518-139">Расположение ресурса частной ссылки.</span><span class="sxs-lookup"><span data-stu-id="36518-139">The Location of Private Link resource.</span></span> <span data-ttu-id="36518-140">При установке PrivateLinkResourceId требуется указать расположение</span><span class="sxs-lookup"><span data-stu-id="36518-140">Location is required when PrivateLinkResourceId is set</span></span>

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

### <span data-ttu-id="36518-141">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="36518-141">-PrivateLinkResourceId</span></span>
<span data-ttu-id="36518-142">Идентификатор ресурса частной ссылки.</span><span class="sxs-lookup"><span data-stu-id="36518-142">The Resource ID of the Private Link.</span></span> <span data-ttu-id="36518-143">Заполнение этого необязательного поля указывает на то, что этот внутренний сервер является "Private"</span><span class="sxs-lookup"><span data-stu-id="36518-143">Populating this optional field indicates that this backend is 'Private'</span></span>

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

### <span data-ttu-id="36518-144">-Weight</span><span class="sxs-lookup"><span data-stu-id="36518-144">-Weight</span></span>
<span data-ttu-id="36518-145">Вес данной конечной точки в целях балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="36518-145">Weight of this endpoint for load balancing purposes.</span></span>
<span data-ttu-id="36518-146">Должно быть в диапазоне от 1 до 1000.</span><span class="sxs-lookup"><span data-stu-id="36518-146">Must be between 1 and 1000.</span></span>
<span data-ttu-id="36518-147">Значение по умолчанию — 50</span><span class="sxs-lookup"><span data-stu-id="36518-147">Default value is 50</span></span>

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

### <span data-ttu-id="36518-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36518-148">CommonParameters</span></span>
<span data-ttu-id="36518-149">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="36518-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36518-150">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="36518-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36518-151">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="36518-151">INPUTS</span></span>

### <span data-ttu-id="36518-152">Ничего</span><span class="sxs-lookup"><span data-stu-id="36518-152">None</span></span>

## <span data-ttu-id="36518-153">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="36518-153">OUTPUTS</span></span>

### <span data-ttu-id="36518-154">Microsoft. Azure. Commands. FrontDoor. Models. PSBackend</span><span class="sxs-lookup"><span data-stu-id="36518-154">Microsoft.Azure.Commands.FrontDoor.Models.PSBackend</span></span>

## <span data-ttu-id="36518-155">Пуск</span><span class="sxs-lookup"><span data-stu-id="36518-155">NOTES</span></span>

## <span data-ttu-id="36518-156">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="36518-156">RELATED LINKS</span></span>

[<span data-ttu-id="36518-157">New-AzFrontDoorBackendPoolObject</span><span class="sxs-lookup"><span data-stu-id="36518-157">New-AzFrontDoorBackendPoolObject</span></span>](./New-AzFrontDoorBackendPoolObject.md)
