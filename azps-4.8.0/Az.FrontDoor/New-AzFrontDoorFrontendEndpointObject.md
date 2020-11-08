---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorfrontendendpointobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorFrontendEndpointObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorFrontendEndpointObject.md
ms.openlocfilehash: efb32f3fa73fac50e5f96100ed895c2ca7d4a83e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244947"
---
# <span data-ttu-id="2154b-101">New-AzFrontDoorFrontendEndpointObject</span><span class="sxs-lookup"><span data-stu-id="2154b-101">New-AzFrontDoorFrontendEndpointObject</span></span>

## <span data-ttu-id="2154b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2154b-102">SYNOPSIS</span></span>
<span data-ttu-id="2154b-103">Создание объекта PSFrontendEndpoint для создания передней дверцы</span><span class="sxs-lookup"><span data-stu-id="2154b-103">Create a PSFrontendEndpoint Object for Front Door creation</span></span>

## <span data-ttu-id="2154b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2154b-104">SYNTAX</span></span>

```
New-AzFrontDoorFrontendEndpointObject -Name <String> -HostName <String>
 [-SessionAffinityEnabledState <PSEnabledState>] [-SessionAffinityTtlInSeconds <Int32>]
 [-WebApplicationFirewallPolicyLink <String>] [-CertificateSource <String>] [-MinimumTlsVersion <String>]
 [-ProtocolType <String>] [-Vault <String>] [-SecretName <String>] [-SecretVersion <String>]
 [-CertificateType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2154b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2154b-105">DESCRIPTION</span></span>
<span data-ttu-id="2154b-106">Создание объекта PSFrontendEndpoint для создания передней дверцы</span><span class="sxs-lookup"><span data-stu-id="2154b-106">Create a PSFrontendEndpoint Object for Front Door creation</span></span>

## <span data-ttu-id="2154b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2154b-107">EXAMPLES</span></span>

### <span data-ttu-id="2154b-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2154b-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorFrontendEndpointObject -Name "frontendendpoint1" -HostName "frontendendpoint1"


HostName                         : frontendendpoint1
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     :
CustomHttpsProvisioningSubstate  :
CertificateSource                :
MinimumTlsVersion                : 1.2
Vault                            :
SecretName                       :
SecretVersion                    :
CertificateType                  :
ResourceState                    :
Id                               :
Name                             : frontendendpoint1
Type                             :
ProtocolType                     : ServerNameIndication
```

<span data-ttu-id="2154b-109">Создайте объект PSFrontendEndpoint для создания передней дверцы.</span><span class="sxs-lookup"><span data-stu-id="2154b-109">Create a PSFrontendEndpoint Object for Front Door creation.</span></span>

## <span data-ttu-id="2154b-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2154b-110">PARAMETERS</span></span>

### <span data-ttu-id="2154b-111">-CertificateSource</span><span class="sxs-lookup"><span data-stu-id="2154b-111">-CertificateSource</span></span>
<span data-ttu-id="2154b-112">Источник SSL-сертификата</span><span class="sxs-lookup"><span data-stu-id="2154b-112">The source of the SSL certificate</span></span>

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

### <span data-ttu-id="2154b-113">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="2154b-113">-CertificateType</span></span>
<span data-ttu-id="2154b-114">тип сертификата, используемого для безопасного соединения с frontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="2154b-114">the type of the certificate used for secure connections to a frontendEndpoint</span></span>

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

### <span data-ttu-id="2154b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2154b-115">-DefaultProfile</span></span>
<span data-ttu-id="2154b-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2154b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2154b-117">-HostName</span><span class="sxs-lookup"><span data-stu-id="2154b-117">-HostName</span></span>
<span data-ttu-id="2154b-118">Имя узла frontendEndpoint.</span><span class="sxs-lookup"><span data-stu-id="2154b-118">The host name of the frontendEndpoint.</span></span>
<span data-ttu-id="2154b-119">Должно быть именем домена.</span><span class="sxs-lookup"><span data-stu-id="2154b-119">Must be a domain name.</span></span>

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

### <span data-ttu-id="2154b-120">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="2154b-120">-MinimumTlsVersion</span></span>
<span data-ttu-id="2154b-121">Минимальная версия TLS, необходимая на клиентах для установления подтверждения SSL с помощью передней дверцы.</span><span class="sxs-lookup"><span data-stu-id="2154b-121">The minimum TLS version required from the clients to establish an SSL handshake with Front Door.</span></span>

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

### <span data-ttu-id="2154b-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2154b-122">-Name</span></span>
<span data-ttu-id="2154b-123">Имя конечной точки переднего плана.</span><span class="sxs-lookup"><span data-stu-id="2154b-123">Frontend endpoint name.</span></span>

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

### <span data-ttu-id="2154b-124">-ProtocolType</span><span class="sxs-lookup"><span data-stu-id="2154b-124">-ProtocolType</span></span>
<span data-ttu-id="2154b-125">Протокол расширения TLS, который используется для безопасной доставки</span><span class="sxs-lookup"><span data-stu-id="2154b-125">The TLS extension protocol that is used for secure delivery</span></span>

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

### <span data-ttu-id="2154b-126">-SecretName</span><span class="sxs-lookup"><span data-stu-id="2154b-126">-SecretName</span></span>
<span data-ttu-id="2154b-127">Имя секрета в хранилище ключей, представляющее полный PFX-сертификат.</span><span class="sxs-lookup"><span data-stu-id="2154b-127">The name of the Key Vault secret representing the full certificate PFX</span></span>

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

### <span data-ttu-id="2154b-128">-SecretVersion</span><span class="sxs-lookup"><span data-stu-id="2154b-128">-SecretVersion</span></span>
<span data-ttu-id="2154b-129">Версия секрета хранилища ключей, представляющая полный PFX-сертификат.</span><span class="sxs-lookup"><span data-stu-id="2154b-129">The version of the Key Vault secret representing the full certificate PFX</span></span>

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

### <span data-ttu-id="2154b-130">-SessionAffinityEnabledState</span><span class="sxs-lookup"><span data-stu-id="2154b-130">-SessionAffinityEnabledState</span></span>
<span data-ttu-id="2154b-131">Разрешено ли сходство сеансов на этом узле.</span><span class="sxs-lookup"><span data-stu-id="2154b-131">Whether to allow session affinity on this host.</span></span>
<span data-ttu-id="2154b-132">Значение по умолчанию отключено</span><span class="sxs-lookup"><span data-stu-id="2154b-132">Default value is Disabled</span></span>

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

### <span data-ttu-id="2154b-133">-SessionAffinityTtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="2154b-133">-SessionAffinityTtlInSeconds</span></span>
<span data-ttu-id="2154b-134">Срок жизни, который будет использоваться в секундах для сходства сеанса (если применимо).</span><span class="sxs-lookup"><span data-stu-id="2154b-134">The TTL to use in seconds for session affinity, if applicable.</span></span> <span data-ttu-id="2154b-135">Значение по умолчанию: 0</span><span class="sxs-lookup"><span data-stu-id="2154b-135">Default value is 0</span></span>

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

### <span data-ttu-id="2154b-136">-Хранилище</span><span class="sxs-lookup"><span data-stu-id="2154b-136">-Vault</span></span>
<span data-ttu-id="2154b-137">Хранилище ключей, содержащее SSL-сертификат</span><span class="sxs-lookup"><span data-stu-id="2154b-137">The Key Vault containing the SSL certificate</span></span>

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

### <span data-ttu-id="2154b-138">-WebApplicationFirewallPolicyLink</span><span class="sxs-lookup"><span data-stu-id="2154b-138">-WebApplicationFirewallPolicyLink</span></span>
<span data-ttu-id="2154b-139">Идентификатор ресурса политики брандмауэра для веб-приложения для каждого узла (если применимо)</span><span class="sxs-lookup"><span data-stu-id="2154b-139">The resource id of Web Application Firewall policy for each host (if applicable)</span></span>

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

### <span data-ttu-id="2154b-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2154b-140">CommonParameters</span></span>
<span data-ttu-id="2154b-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2154b-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2154b-142">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2154b-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2154b-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2154b-143">INPUTS</span></span>

### <span data-ttu-id="2154b-144">Ничего</span><span class="sxs-lookup"><span data-stu-id="2154b-144">None</span></span>
## <span data-ttu-id="2154b-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2154b-145">OUTPUTS</span></span>

### <span data-ttu-id="2154b-146">Microsoft. Azure. Commands. FrontDoor. Models. PSFrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="2154b-146">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span></span>
## <span data-ttu-id="2154b-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="2154b-147">NOTES</span></span>

## <span data-ttu-id="2154b-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2154b-148">RELATED LINKS</span></span>

<span data-ttu-id="2154b-149">[New-AzFrontDoor](./New-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="2154b-149">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)</span></span>
