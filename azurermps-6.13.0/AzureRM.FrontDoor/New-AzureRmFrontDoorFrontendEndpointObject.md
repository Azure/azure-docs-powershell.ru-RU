---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/new-azurermfrontdoorfrontendendpointobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorFrontendEndpointObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorFrontendEndpointObject.md
ms.openlocfilehash: 638617cfe55e01121b46c7fe283d3664948e76b5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93556640"
---
# <span data-ttu-id="03bc2-101">New-AzureRmFrontDoorFrontendEndpointObject</span><span class="sxs-lookup"><span data-stu-id="03bc2-101">New-AzureRmFrontDoorFrontendEndpointObject</span></span>

## <span data-ttu-id="03bc2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="03bc2-102">SYNOPSIS</span></span>
<span data-ttu-id="03bc2-103">Создание объекта PSFrontendEndpoint для создания передней дверцы</span><span class="sxs-lookup"><span data-stu-id="03bc2-103">Create a PSFrontendEndpoint Object for Front Door creation</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="03bc2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="03bc2-104">SYNTAX</span></span>

```
New-AzureRmFrontDoorFrontendEndpointObject -Name <String> -HostName <String>
 [-SessionAffinityEnabledState <PSEnabledState>] [-SessionAffinityTtlInSeconds <Int32>]
 [-WebApplicationFirewallPolicyLink <String>] [-CertificateSource <PSCertificateSource>]
 [-ProtocolType <PSProtocolType>] [-Vault <String>] [-SecretName <String>] [-SecretVersion <String>]
 [-CertificateType <PSCertificateType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="03bc2-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="03bc2-105">DESCRIPTION</span></span>
<span data-ttu-id="03bc2-106">Создание объекта PSFrontendEndpoint для создания передней дверцы</span><span class="sxs-lookup"><span data-stu-id="03bc2-106">Create a PSFrontendEndpoint Object for Front Door creation</span></span>

## <span data-ttu-id="03bc2-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="03bc2-107">EXAMPLES</span></span>

### <span data-ttu-id="03bc2-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="03bc2-108">Example 1</span></span>
```powershell
PS C:\> New-AzureRmFrontDoorFrontendEndpointObject -Name "frontendendpoint1" -HostName $hostName


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

<span data-ttu-id="03bc2-109">Создание объекта PSFrontendEndpoint для создания передней дверцы</span><span class="sxs-lookup"><span data-stu-id="03bc2-109">Create a PSFrontendEndpoint Object for Front Door creation</span></span>

## <span data-ttu-id="03bc2-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="03bc2-110">PARAMETERS</span></span>

### <span data-ttu-id="03bc2-111">-CertificateSource</span><span class="sxs-lookup"><span data-stu-id="03bc2-111">-CertificateSource</span></span>
<span data-ttu-id="03bc2-112">Источник SSL-сертификата</span><span class="sxs-lookup"><span data-stu-id="03bc2-112">The source of the SSL certificate</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSCertificateSource
Parameter Sets: (All)
Aliases:
Accepted values: AzureKeyVault, FrontDoor

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03bc2-113">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="03bc2-113">-CertificateType</span></span>
<span data-ttu-id="03bc2-114">тип сертификата, используемого для безопасного соединения с frontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="03bc2-114">the type of the certificate used for secure connections to a frontendEndpoint</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSCertificateType
Parameter Sets: (All)
Aliases:
Accepted values: Shared, Dedicated

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03bc2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03bc2-115">-DefaultProfile</span></span>
<span data-ttu-id="03bc2-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="03bc2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="03bc2-117">-HostName</span><span class="sxs-lookup"><span data-stu-id="03bc2-117">-HostName</span></span>
<span data-ttu-id="03bc2-118">Имя узла frontendEndpoint.</span><span class="sxs-lookup"><span data-stu-id="03bc2-118">The host name of the frontendEndpoint.</span></span>
<span data-ttu-id="03bc2-119">Должно быть именем домена.</span><span class="sxs-lookup"><span data-stu-id="03bc2-119">Must be a domain name.</span></span>

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

### <span data-ttu-id="03bc2-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="03bc2-120">-Name</span></span>
<span data-ttu-id="03bc2-121">Имя конечной точки переднего плана.</span><span class="sxs-lookup"><span data-stu-id="03bc2-121">Frontend endpoint name.</span></span>

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

### <span data-ttu-id="03bc2-122">-ProtocolType</span><span class="sxs-lookup"><span data-stu-id="03bc2-122">-ProtocolType</span></span>
<span data-ttu-id="03bc2-123">Протокол расширения TLS, который используется для безопасной доставки</span><span class="sxs-lookup"><span data-stu-id="03bc2-123">The TLS extension protocol that is used for secure delivery</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSProtocolType
Parameter Sets: (All)
Aliases:
Accepted values: ServerNameIndication, IPBased

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03bc2-124">-SecretName</span><span class="sxs-lookup"><span data-stu-id="03bc2-124">-SecretName</span></span>
<span data-ttu-id="03bc2-125">Имя секрета в хранилище ключей, представляющее полный PFX-сертификат.</span><span class="sxs-lookup"><span data-stu-id="03bc2-125">The name of the Key Vault secret representing the full certificate PFX</span></span>

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

### <span data-ttu-id="03bc2-126">-SecretVersion</span><span class="sxs-lookup"><span data-stu-id="03bc2-126">-SecretVersion</span></span>
<span data-ttu-id="03bc2-127">Версия секрета хранилища ключей, представляющая полный PFX-сертификат.</span><span class="sxs-lookup"><span data-stu-id="03bc2-127">The version of the Key Vault secret representing the full certificate PFX</span></span>

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

### <span data-ttu-id="03bc2-128">-SessionAffinityEnabledState</span><span class="sxs-lookup"><span data-stu-id="03bc2-128">-SessionAffinityEnabledState</span></span>
<span data-ttu-id="03bc2-129">Разрешено ли сходство сеансов на этом узле.</span><span class="sxs-lookup"><span data-stu-id="03bc2-129">Whether to allow session affinity on this host.</span></span>
<span data-ttu-id="03bc2-130">Значение по умолчанию отключено</span><span class="sxs-lookup"><span data-stu-id="03bc2-130">Default value is Disabled</span></span>

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

### <span data-ttu-id="03bc2-131">-SessionAffinityTtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="03bc2-131">-SessionAffinityTtlInSeconds</span></span>
<span data-ttu-id="03bc2-132">Срок жизни, который будет использоваться в секундах для сходства сеанса (если применимо).</span><span class="sxs-lookup"><span data-stu-id="03bc2-132">The TTL to use in seconds for session affinity, if applicable.</span></span> <span data-ttu-id="03bc2-133">Значение по умолчанию: 0</span><span class="sxs-lookup"><span data-stu-id="03bc2-133">Default value is 0</span></span>

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

### <span data-ttu-id="03bc2-134">-Хранилище</span><span class="sxs-lookup"><span data-stu-id="03bc2-134">-Vault</span></span>
<span data-ttu-id="03bc2-135">Хранилище ключей, содержащее SSL-сертификат</span><span class="sxs-lookup"><span data-stu-id="03bc2-135">The Key Vault containing the SSL certificate</span></span>

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

### <span data-ttu-id="03bc2-136">-WebApplicationFirewallPolicyLink</span><span class="sxs-lookup"><span data-stu-id="03bc2-136">-WebApplicationFirewallPolicyLink</span></span>
<span data-ttu-id="03bc2-137">Идентификатор ресурса политики брандмауэра для веб-приложения для каждого узла (если применимо)</span><span class="sxs-lookup"><span data-stu-id="03bc2-137">The resource id of Web Application Firewall policy for each host (if applicable)</span></span>

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

### <span data-ttu-id="03bc2-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03bc2-138">CommonParameters</span></span>
<span data-ttu-id="03bc2-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="03bc2-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03bc2-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03bc2-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03bc2-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="03bc2-141">INPUTS</span></span>

### <span data-ttu-id="03bc2-142">Ничего</span><span class="sxs-lookup"><span data-stu-id="03bc2-142">None</span></span>

## <span data-ttu-id="03bc2-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="03bc2-143">OUTPUTS</span></span>

### <span data-ttu-id="03bc2-144">Microsoft. Azure. Commands. FrontDoor. Models. PSFrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="03bc2-144">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span></span>

## <span data-ttu-id="03bc2-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="03bc2-145">NOTES</span></span>

## <span data-ttu-id="03bc2-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="03bc2-146">RELATED LINKS</span></span>

<span data-ttu-id="03bc2-147">[New-AzureRmFrontDoor](./New-AzureRmFrontDoor.md) 
 [Set-AzureRmFrontDoor](./Set-AzureRmFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="03bc2-147">[New-AzureRmFrontDoor](./New-AzureRmFrontDoor.md)
[Set-AzureRmFrontDoor](./Set-AzureRmFrontDoor.md)</span></span>
