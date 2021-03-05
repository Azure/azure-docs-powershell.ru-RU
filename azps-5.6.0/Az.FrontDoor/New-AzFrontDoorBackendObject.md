---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/new-azfrontdoorbackendobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendObject.md
ms.openlocfilehash: d5b7a2d0713fec7c11f33d778cf9708c253f153a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101965912"
---
# <span data-ttu-id="93efa-101">New-AzFrontDoorBackendObject</span><span class="sxs-lookup"><span data-stu-id="93efa-101">New-AzFrontDoorBackendObject</span></span>

## <span data-ttu-id="93efa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="93efa-102">SYNOPSIS</span></span>
<span data-ttu-id="93efa-103">Создание объекта PSBackend</span><span class="sxs-lookup"><span data-stu-id="93efa-103">Create a PSBackend object</span></span>

## <span data-ttu-id="93efa-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="93efa-104">SYNTAX</span></span>

```
New-AzFrontDoorBackendObject -Address <String> [-HttpPort <Int32>] [-HttpsPort <Int32>] [-Priority <Int32>]
 [-Weight <Int32>] [-EnabledState <PSEnabledState>] [-BackendHostHeader <String>] [-PrivateLinkAlias <String>]
 [-PrivateLinkResourceId <String>] [-PrivateLinkLocation <String>] [-PrivateLinkApprovalMessage <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="93efa-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="93efa-105">DESCRIPTION</span></span>
<span data-ttu-id="93efa-106">Создание объекта PSBackend для создания передней двери</span><span class="sxs-lookup"><span data-stu-id="93efa-106">Create a PSBackend object for Front Door creation</span></span>

## <span data-ttu-id="93efa-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="93efa-107">EXAMPLES</span></span>

### <span data-ttu-id="93efa-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="93efa-108">Example 1</span></span>
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

<span data-ttu-id="93efa-109">Создание объекта PSBackend для создания передней двери</span><span class="sxs-lookup"><span data-stu-id="93efa-109">Create a PSBackend object for Front Door creation</span></span>

## <span data-ttu-id="93efa-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="93efa-110">PARAMETERS</span></span>

### <span data-ttu-id="93efa-111">-Address</span><span class="sxs-lookup"><span data-stu-id="93efa-111">-Address</span></span>
<span data-ttu-id="93efa-112">Расположение backend (IP-адрес или FQDN)</span><span class="sxs-lookup"><span data-stu-id="93efa-112">Location of the backend (IP address or FQDN)</span></span>

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

### <span data-ttu-id="93efa-113">-BackendHostHeader</span><span class="sxs-lookup"><span data-stu-id="93efa-113">-BackendHostHeader</span></span>
<span data-ttu-id="93efa-114">Значение, используемого в качестве загона хоста, относящегося к backend.</span><span class="sxs-lookup"><span data-stu-id="93efa-114">The value to use as the host header sent to the backend.</span></span> <span data-ttu-id="93efa-115">Значением по умолчанию является адрес задней почты.</span><span class="sxs-lookup"><span data-stu-id="93efa-115">Default value is the backend address.</span></span>

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

### <span data-ttu-id="93efa-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93efa-116">-DefaultProfile</span></span>
<span data-ttu-id="93efa-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="93efa-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="93efa-118">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="93efa-118">-EnabledState</span></span>
<span data-ttu-id="93efa-119">Следует ли включить использование этого backend.</span><span class="sxs-lookup"><span data-stu-id="93efa-119">Whether to enable use of this backend.</span></span> <span data-ttu-id="93efa-120">Значение по умолчанию включено</span><span class="sxs-lookup"><span data-stu-id="93efa-120">Default value is Enabled</span></span>

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

### <span data-ttu-id="93efa-121">-httpPort</span><span class="sxs-lookup"><span data-stu-id="93efa-121">-HttpPort</span></span>
<span data-ttu-id="93efa-122">Номер порта HTTP TCP.</span><span class="sxs-lookup"><span data-stu-id="93efa-122">The HTTP TCP port number.</span></span>
<span data-ttu-id="93efa-123">Должен быть в период от 1 до 65 535.</span><span class="sxs-lookup"><span data-stu-id="93efa-123">Must be between 1 and 65535.</span></span>
<span data-ttu-id="93efa-124">Значение по умолчанию — 80.</span><span class="sxs-lookup"><span data-stu-id="93efa-124">Default value is 80.</span></span>

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

### <span data-ttu-id="93efa-125">-HttpsPort</span><span class="sxs-lookup"><span data-stu-id="93efa-125">-HttpsPort</span></span>
<span data-ttu-id="93efa-126">Номер порта TCP HTTPS.</span><span class="sxs-lookup"><span data-stu-id="93efa-126">The HTTPS TCP port number.</span></span>
<span data-ttu-id="93efa-127">Должен быть в период от 1 до 65 535.</span><span class="sxs-lookup"><span data-stu-id="93efa-127">Must be between 1 and 65535.</span></span>
<span data-ttu-id="93efa-128">Значение по умолчанию — 443</span><span class="sxs-lookup"><span data-stu-id="93efa-128">Default value is 443</span></span>

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

### <span data-ttu-id="93efa-129">-Priority</span><span class="sxs-lookup"><span data-stu-id="93efa-129">-Priority</span></span>
<span data-ttu-id="93efa-130">Приоритет балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="93efa-130">Priority to use for load balancing.</span></span>
<span data-ttu-id="93efa-131">Должен быть от 1 до 5.</span><span class="sxs-lookup"><span data-stu-id="93efa-131">Must be between 1 and 5.</span></span>
<span data-ttu-id="93efa-132">Значение по умолчанию — 1</span><span class="sxs-lookup"><span data-stu-id="93efa-132">Default value is 1</span></span>

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

### <span data-ttu-id="93efa-133">-PrivateLinkAlias</span><span class="sxs-lookup"><span data-stu-id="93efa-133">-PrivateLinkAlias</span></span>
<span data-ttu-id="93efa-134">Псевдоним ресурса Private Link.</span><span class="sxs-lookup"><span data-stu-id="93efa-134">The Alias of the Private Link resource.</span></span> <span data-ttu-id="93efa-135">Заполнение этого необязательного поля указывает на то, что это backend is private (Частное).</span><span class="sxs-lookup"><span data-stu-id="93efa-135">Populating this optional field indicates that this backend is 'Private'</span></span>

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

### <span data-ttu-id="93efa-136">-PrivateLinkApprovalMessage</span><span class="sxs-lookup"><span data-stu-id="93efa-136">-PrivateLinkApprovalMessage</span></span>
<span data-ttu-id="93efa-137">Пользовательское сообщение, которое будет включено в запрос на утверждение для подключения к личной ссылке</span><span class="sxs-lookup"><span data-stu-id="93efa-137">A custom message to be included in the approval request to connect to the Private Link</span></span>

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

### <span data-ttu-id="93efa-138">-PrivateLinkLocation</span><span class="sxs-lookup"><span data-stu-id="93efa-138">-PrivateLinkLocation</span></span>
<span data-ttu-id="93efa-139">Расположение ресурса private Link.</span><span class="sxs-lookup"><span data-stu-id="93efa-139">The Location of Private Link resource.</span></span> <span data-ttu-id="93efa-140">Расположение является требоваться, если задан PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="93efa-140">Location is required when PrivateLinkResourceId is set</span></span>

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

### <span data-ttu-id="93efa-141">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="93efa-141">-PrivateLinkResourceId</span></span>
<span data-ttu-id="93efa-142">ИД ресурса личной ссылки.</span><span class="sxs-lookup"><span data-stu-id="93efa-142">The Resource ID of the Private Link.</span></span> <span data-ttu-id="93efa-143">Заполнение этого необязательного поля указывает на то, что это backend is private (Частное).</span><span class="sxs-lookup"><span data-stu-id="93efa-143">Populating this optional field indicates that this backend is 'Private'</span></span>

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

### <span data-ttu-id="93efa-144">-Weight</span><span class="sxs-lookup"><span data-stu-id="93efa-144">-Weight</span></span>
<span data-ttu-id="93efa-145">Вес этой конечной точки для целей балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="93efa-145">Weight of this endpoint for load balancing purposes.</span></span>
<span data-ttu-id="93efa-146">Должно быть от 1 до 1000.</span><span class="sxs-lookup"><span data-stu-id="93efa-146">Must be between 1 and 1000.</span></span>
<span data-ttu-id="93efa-147">Значение по умолчанию — 50</span><span class="sxs-lookup"><span data-stu-id="93efa-147">Default value is 50</span></span>

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

### <span data-ttu-id="93efa-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93efa-148">CommonParameters</span></span>
<span data-ttu-id="93efa-149">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93efa-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93efa-150">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="93efa-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93efa-151">INPUTS</span><span class="sxs-lookup"><span data-stu-id="93efa-151">INPUTS</span></span>

### <span data-ttu-id="93efa-152">Нет</span><span class="sxs-lookup"><span data-stu-id="93efa-152">None</span></span>

## <span data-ttu-id="93efa-153">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="93efa-153">OUTPUTS</span></span>

### <span data-ttu-id="93efa-154">Microsoft.Azure.Commands.FrontDoor.Models.PSBackend</span><span class="sxs-lookup"><span data-stu-id="93efa-154">Microsoft.Azure.Commands.FrontDoor.Models.PSBackend</span></span>

## <span data-ttu-id="93efa-155">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="93efa-155">NOTES</span></span>

## <span data-ttu-id="93efa-156">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="93efa-156">RELATED LINKS</span></span>

[<span data-ttu-id="93efa-157">New-AzFrontDoorBackendPoolObject</span><span class="sxs-lookup"><span data-stu-id="93efa-157">New-AzFrontDoorBackendPoolObject</span></span>](./New-AzFrontDoorBackendPoolObject.md)
