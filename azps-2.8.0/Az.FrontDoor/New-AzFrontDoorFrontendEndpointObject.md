---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorfrontendendpointobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorFrontendEndpointObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorFrontendEndpointObject.md
ms.openlocfilehash: 3684c7d0cf28c0814178ea234f9368d138fc78d8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720894"
---
# <span data-ttu-id="4e0a7-101">New-AzFrontDoorFrontendEndpointObject</span><span class="sxs-lookup"><span data-stu-id="4e0a7-101">New-AzFrontDoorFrontendEndpointObject</span></span>

## <span data-ttu-id="4e0a7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4e0a7-102">SYNOPSIS</span></span>
<span data-ttu-id="4e0a7-103">Создание объекта PSFrontendEndpoint для создания передней дверцы</span><span class="sxs-lookup"><span data-stu-id="4e0a7-103">Create a PSFrontendEndpoint Object for Front Door creation</span></span>

## <span data-ttu-id="4e0a7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4e0a7-104">SYNTAX</span></span>

```
New-AzFrontDoorFrontendEndpointObject -Name <String> -HostName <String>
 [-SessionAffinityEnabledState <PSEnabledState>] [-SessionAffinityTtlInSeconds <Int32>]
 [-WebApplicationFirewallPolicyLink <String>] [-CertificateSource <String>] [-ProtocolType <String>]
 [-Vault <String>] [-SecretName <String>] [-SecretVersion <String>] [-CertificateType <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4e0a7-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4e0a7-105">DESCRIPTION</span></span>
<span data-ttu-id="4e0a7-106">Создание объекта PSFrontendEndpoint для создания передней дверцы</span><span class="sxs-lookup"><span data-stu-id="4e0a7-106">Create a PSFrontendEndpoint Object for Front Door creation</span></span>

## <span data-ttu-id="4e0a7-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4e0a7-107">EXAMPLES</span></span>

### <span data-ttu-id="4e0a7-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4e0a7-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorFrontendEndpointObject -Name "frontendendpoint1" -HostName $hostName


HostName                         : frontdoor5.azurefd.net
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     :
CustomHttpsProvisioningSubstate  :
CertificateSource                : AzureKeyVault
ProtocolType                     : ServerNameIndication
Vault                            :
SecretName                       :
SecretVersion                    :
CertificateType                  : Shared
ResourceState                    :
Id                               :
Name                             : frontendendpoint1
Type                             :
```

<span data-ttu-id="4e0a7-109">Создание объекта PSFrontendEndpoint для создания передней дверцы</span><span class="sxs-lookup"><span data-stu-id="4e0a7-109">Create a PSFrontendEndpoint Object for Front Door creation</span></span>

## <span data-ttu-id="4e0a7-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4e0a7-110">PARAMETERS</span></span>

### <span data-ttu-id="4e0a7-111">-CertificateSource</span><span class="sxs-lookup"><span data-stu-id="4e0a7-111">-CertificateSource</span></span>
<span data-ttu-id="4e0a7-112">Источник SSL-сертификата</span><span class="sxs-lookup"><span data-stu-id="4e0a7-112">The source of the SSL certificate</span></span>

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

### <span data-ttu-id="4e0a7-113">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="4e0a7-113">-CertificateType</span></span>
<span data-ttu-id="4e0a7-114">тип сертификата, используемого для безопасного соединения с frontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="4e0a7-114">the type of the certificate used for secure connections to a frontendEndpoint</span></span>

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

### <span data-ttu-id="4e0a7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e0a7-115">-DefaultProfile</span></span>
<span data-ttu-id="4e0a7-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4e0a7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e0a7-117">-HostName</span><span class="sxs-lookup"><span data-stu-id="4e0a7-117">-HostName</span></span>
<span data-ttu-id="4e0a7-118">Имя узла frontendEndpoint.</span><span class="sxs-lookup"><span data-stu-id="4e0a7-118">The host name of the frontendEndpoint.</span></span>
<span data-ttu-id="4e0a7-119">Должно быть именем домена.</span><span class="sxs-lookup"><span data-stu-id="4e0a7-119">Must be a domain name.</span></span>

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

### <span data-ttu-id="4e0a7-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4e0a7-120">-Name</span></span>
<span data-ttu-id="4e0a7-121">Имя конечной точки переднего плана.</span><span class="sxs-lookup"><span data-stu-id="4e0a7-121">Frontend endpoint name.</span></span>

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

### <span data-ttu-id="4e0a7-122">-ProtocolType</span><span class="sxs-lookup"><span data-stu-id="4e0a7-122">-ProtocolType</span></span>
<span data-ttu-id="4e0a7-123">Протокол расширения TLS, который используется для безопасной доставки</span><span class="sxs-lookup"><span data-stu-id="4e0a7-123">The TLS extension protocol that is used for secure delivery</span></span>

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

### <span data-ttu-id="4e0a7-124">-SecretName</span><span class="sxs-lookup"><span data-stu-id="4e0a7-124">-SecretName</span></span>
<span data-ttu-id="4e0a7-125">Имя секрета в хранилище ключей, представляющее полный PFX-сертификат.</span><span class="sxs-lookup"><span data-stu-id="4e0a7-125">The name of the Key Vault secret representing the full certificate PFX</span></span>

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

### <span data-ttu-id="4e0a7-126">-SecretVersion</span><span class="sxs-lookup"><span data-stu-id="4e0a7-126">-SecretVersion</span></span>
<span data-ttu-id="4e0a7-127">Версия секрета хранилища ключей, представляющая полный PFX-сертификат.</span><span class="sxs-lookup"><span data-stu-id="4e0a7-127">The version of the Key Vault secret representing the full certificate PFX</span></span>

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

### <span data-ttu-id="4e0a7-128">-SessionAffinityEnabledState</span><span class="sxs-lookup"><span data-stu-id="4e0a7-128">-SessionAffinityEnabledState</span></span>
<span data-ttu-id="4e0a7-129">Разрешено ли сходство сеансов на этом узле.</span><span class="sxs-lookup"><span data-stu-id="4e0a7-129">Whether to allow session affinity on this host.</span></span>
<span data-ttu-id="4e0a7-130">Значение по умолчанию отключено</span><span class="sxs-lookup"><span data-stu-id="4e0a7-130">Default value is Disabled</span></span>

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

### <span data-ttu-id="4e0a7-131">-SessionAffinityTtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="4e0a7-131">-SessionAffinityTtlInSeconds</span></span>
<span data-ttu-id="4e0a7-132">Срок жизни, который будет использоваться в секундах для сходства сеанса (если применимо).</span><span class="sxs-lookup"><span data-stu-id="4e0a7-132">The TTL to use in seconds for session affinity, if applicable.</span></span> <span data-ttu-id="4e0a7-133">Значение по умолчанию: 0</span><span class="sxs-lookup"><span data-stu-id="4e0a7-133">Default value is 0</span></span>

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

### <span data-ttu-id="4e0a7-134">-Хранилище</span><span class="sxs-lookup"><span data-stu-id="4e0a7-134">-Vault</span></span>
<span data-ttu-id="4e0a7-135">Хранилище ключей, содержащее SSL-сертификат</span><span class="sxs-lookup"><span data-stu-id="4e0a7-135">The Key Vault containing the SSL certificate</span></span>

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

### <span data-ttu-id="4e0a7-136">-WebApplicationFirewallPolicyLink</span><span class="sxs-lookup"><span data-stu-id="4e0a7-136">-WebApplicationFirewallPolicyLink</span></span>
<span data-ttu-id="4e0a7-137">Идентификатор ресурса политики брандмауэра для веб-приложения для каждого узла (если применимо)</span><span class="sxs-lookup"><span data-stu-id="4e0a7-137">The resource id of Web Application Firewall policy for each host (if applicable)</span></span>

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

### <span data-ttu-id="4e0a7-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e0a7-138">CommonParameters</span></span>
<span data-ttu-id="4e0a7-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4e0a7-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e0a7-140">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4e0a7-140">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e0a7-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4e0a7-141">INPUTS</span></span>

### <span data-ttu-id="4e0a7-142">Ничего</span><span class="sxs-lookup"><span data-stu-id="4e0a7-142">None</span></span>

## <span data-ttu-id="4e0a7-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4e0a7-143">OUTPUTS</span></span>

### <span data-ttu-id="4e0a7-144">Microsoft. Azure. Commands. FrontDoor. Models. PSFrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="4e0a7-144">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span></span>

## <span data-ttu-id="4e0a7-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="4e0a7-145">NOTES</span></span>

## <span data-ttu-id="4e0a7-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4e0a7-146">RELATED LINKS</span></span>

<span data-ttu-id="4e0a7-147">[New-AzFrontDoor](./New-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="4e0a7-147">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)</span></span>
