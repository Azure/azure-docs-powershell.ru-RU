---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorfrontendendpointobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorFrontendEndpointObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorFrontendEndpointObject.md
ms.openlocfilehash: efb32f3fa73fac50e5f96100ed895c2ca7d4a83e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98326427"
---
# <span data-ttu-id="e1c2f-101">New-AzFrontDoorFrontendEndpointObject</span><span class="sxs-lookup"><span data-stu-id="e1c2f-101">New-AzFrontDoorFrontendEndpointObject</span></span>

## <span data-ttu-id="e1c2f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e1c2f-102">SYNOPSIS</span></span>
<span data-ttu-id="e1c2f-103">Создание объекта PSFrontendEndpoint для создания передней двери</span><span class="sxs-lookup"><span data-stu-id="e1c2f-103">Create a PSFrontendEndpoint Object for Front Door creation</span></span>

## <span data-ttu-id="e1c2f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e1c2f-104">SYNTAX</span></span>

```
New-AzFrontDoorFrontendEndpointObject -Name <String> -HostName <String>
 [-SessionAffinityEnabledState <PSEnabledState>] [-SessionAffinityTtlInSeconds <Int32>]
 [-WebApplicationFirewallPolicyLink <String>] [-CertificateSource <String>] [-MinimumTlsVersion <String>]
 [-ProtocolType <String>] [-Vault <String>] [-SecretName <String>] [-SecretVersion <String>]
 [-CertificateType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e1c2f-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e1c2f-105">DESCRIPTION</span></span>
<span data-ttu-id="e1c2f-106">Создание объекта PSFrontendEndpoint для создания передней двери</span><span class="sxs-lookup"><span data-stu-id="e1c2f-106">Create a PSFrontendEndpoint Object for Front Door creation</span></span>

## <span data-ttu-id="e1c2f-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e1c2f-107">EXAMPLES</span></span>

### <span data-ttu-id="e1c2f-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e1c2f-108">Example 1</span></span>
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

<span data-ttu-id="e1c2f-109">Создайте объект PSFrontendEndpoint для создания передней двери.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-109">Create a PSFrontendEndpoint Object for Front Door creation.</span></span>

## <span data-ttu-id="e1c2f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e1c2f-110">PARAMETERS</span></span>

### <span data-ttu-id="e1c2f-111">-CertificateSource</span><span class="sxs-lookup"><span data-stu-id="e1c2f-111">-CertificateSource</span></span>
<span data-ttu-id="e1c2f-112">Источник SSL-сертификата</span><span class="sxs-lookup"><span data-stu-id="e1c2f-112">The source of the SSL certificate</span></span>

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

### <span data-ttu-id="e1c2f-113">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="e1c2f-113">-CertificateType</span></span>
<span data-ttu-id="e1c2f-114">Тип сертификата, используемого для безопасных подключений к frontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="e1c2f-114">the type of the certificate used for secure connections to a frontendEndpoint</span></span>

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

### <span data-ttu-id="e1c2f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1c2f-115">-DefaultProfile</span></span>
<span data-ttu-id="e1c2f-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e1c2f-117">-HostName</span><span class="sxs-lookup"><span data-stu-id="e1c2f-117">-HostName</span></span>
<span data-ttu-id="e1c2f-118">Имя host of the frontendEndpoint.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-118">The host name of the frontendEndpoint.</span></span>
<span data-ttu-id="e1c2f-119">Должен быть доменным именем.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-119">Must be a domain name.</span></span>

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

### <span data-ttu-id="e1c2f-120">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="e1c2f-120">-MinimumTlsVersion</span></span>
<span data-ttu-id="e1c2f-121">Минимальная версия TLS, необходимая клиентам для того, чтобы получить SSL-handshake with Front Door.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-121">The minimum TLS version required from the clients to establish an SSL handshake with Front Door.</span></span>

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

### <span data-ttu-id="e1c2f-122">-Name</span><span class="sxs-lookup"><span data-stu-id="e1c2f-122">-Name</span></span>
<span data-ttu-id="e1c2f-123">Имя конечной точки frontend.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-123">Frontend endpoint name.</span></span>

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

### <span data-ttu-id="e1c2f-124">-ProtocolType</span><span class="sxs-lookup"><span data-stu-id="e1c2f-124">-ProtocolType</span></span>
<span data-ttu-id="e1c2f-125">Протокол расширения TLS, используемый для безопасной доставки</span><span class="sxs-lookup"><span data-stu-id="e1c2f-125">The TLS extension protocol that is used for secure delivery</span></span>

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

### <span data-ttu-id="e1c2f-126">-SecretName</span><span class="sxs-lookup"><span data-stu-id="e1c2f-126">-SecretName</span></span>
<span data-ttu-id="e1c2f-127">Имя секретного сейфа ключа, представляющее полный сертификат PFX</span><span class="sxs-lookup"><span data-stu-id="e1c2f-127">The name of the Key Vault secret representing the full certificate PFX</span></span>

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

### <span data-ttu-id="e1c2f-128">-SecretVersion</span><span class="sxs-lookup"><span data-stu-id="e1c2f-128">-SecretVersion</span></span>
<span data-ttu-id="e1c2f-129">Версия секретного сейфа ключа, представляющая полный сертификат PFX</span><span class="sxs-lookup"><span data-stu-id="e1c2f-129">The version of the Key Vault secret representing the full certificate PFX</span></span>

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

### <span data-ttu-id="e1c2f-130">-SessionAffinityEnabledState</span><span class="sxs-lookup"><span data-stu-id="e1c2f-130">-SessionAffinityEnabledState</span></span>
<span data-ttu-id="e1c2f-131">Разрешить ли сеансы сходства для этого хоста.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-131">Whether to allow session affinity on this host.</span></span>
<span data-ttu-id="e1c2f-132">Значение по умолчанию отключено</span><span class="sxs-lookup"><span data-stu-id="e1c2f-132">Default value is Disabled</span></span>

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

### <span data-ttu-id="e1c2f-133">-SessionAffinityTtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="e1c2f-133">-SessionAffinityTtlInSeconds</span></span>
<span data-ttu-id="e1c2f-134">TTL, который используется в секундах для сходства сеанса, если применимо.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-134">The TTL to use in seconds for session affinity, if applicable.</span></span> <span data-ttu-id="e1c2f-135">Значение по умолчанию — 0</span><span class="sxs-lookup"><span data-stu-id="e1c2f-135">Default value is 0</span></span>

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

### <span data-ttu-id="e1c2f-136">-Vault</span><span class="sxs-lookup"><span data-stu-id="e1c2f-136">-Vault</span></span>
<span data-ttu-id="e1c2f-137">Хранилище ключей, содержащее SSL-сертификат</span><span class="sxs-lookup"><span data-stu-id="e1c2f-137">The Key Vault containing the SSL certificate</span></span>

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

### <span data-ttu-id="e1c2f-138">-WebApplicationFirewallPolicyLink</span><span class="sxs-lookup"><span data-stu-id="e1c2f-138">-WebApplicationFirewallPolicyLink</span></span>
<span data-ttu-id="e1c2f-139">ИД ресурса политики брандмауэра веб-приложения для каждого хоста (если применимо)</span><span class="sxs-lookup"><span data-stu-id="e1c2f-139">The resource id of Web Application Firewall policy for each host (if applicable)</span></span>

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

### <span data-ttu-id="e1c2f-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1c2f-140">CommonParameters</span></span>
<span data-ttu-id="e1c2f-141">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1c2f-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1c2f-142">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e1c2f-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1c2f-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e1c2f-143">INPUTS</span></span>

### <span data-ttu-id="e1c2f-144">Нет</span><span class="sxs-lookup"><span data-stu-id="e1c2f-144">None</span></span>
## <span data-ttu-id="e1c2f-145">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e1c2f-145">OUTPUTS</span></span>

### <span data-ttu-id="e1c2f-146">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="e1c2f-146">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span></span>
## <span data-ttu-id="e1c2f-147">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e1c2f-147">NOTES</span></span>

## <span data-ttu-id="e1c2f-148">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e1c2f-148">RELATED LINKS</span></span>

<span data-ttu-id="e1c2f-149">[New-AzFrontDoor](./New-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="e1c2f-149">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)</span></span>
