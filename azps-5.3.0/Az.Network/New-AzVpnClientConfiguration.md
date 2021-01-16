---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnclientconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientConfiguration.md
ms.openlocfilehash: 11b18f0a0f12a82e88694fd91ce89956951a4eb6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98421620"
---
# <span data-ttu-id="c6d8e-101">New-AzVpnClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="c6d8e-101">New-AzVpnClientConfiguration</span></span>

## <span data-ttu-id="c6d8e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c6d8e-102">SYNOPSIS</span></span>
<span data-ttu-id="c6d8e-103">Эта команда позволяет пользователям создавать пакет профиля VPN на основе предварительно настроенных параметров VPN-шлюза, а также настраивать некоторые дополнительные параметры, например некоторые корневые сертификаты.</span><span class="sxs-lookup"><span data-stu-id="c6d8e-103">This command allows the users to create the Vpn profile package based on pre-configured vpn settings on the VPN gateway, in addition to some additional settings that users may need to configure, for e.g. some root certificates.</span></span>

## <span data-ttu-id="c6d8e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c6d8e-104">SYNTAX</span></span>

```
New-AzVpnClientConfiguration [-Name <String>] -ResourceGroupName <String> [-ProcessorArchitecture <String>]
 [-AuthenticationMethod <String>] [-RadiusRootCertificateFile <String>]
 [-ClientRootCertificateFileList <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c6d8e-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c6d8e-105">DESCRIPTION</span></span>
<span data-ttu-id="c6d8e-106">это позволит пользователям создавать пакет профиля VPN на основе предварительно настроенных параметров VPN на VPN-шлюзе, а также настраивать некоторые дополнительные параметры, например некоторые корневые сертификаты.</span><span class="sxs-lookup"><span data-stu-id="c6d8e-106">this allows the users to create the Vpn profile package based on pre-configured vpn settings on the VPN gateway, in addition to some additional settings that users may need to configure, for e.g. some root certificates.</span></span>

## <span data-ttu-id="c6d8e-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c6d8e-107">EXAMPLES</span></span>

### <span data-ttu-id="c6d8e-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c6d8e-108">Example 1</span></span>
```
PS C:\> New-AzVpnClientConfiguration -ResourceGroupName "ContosoResourceGroup" -Name "ContosoVirtualNetworkGateway" -AuthenticationMethod "EAPTLS" -RadiusRootCertificateFile "C:\Users\Test\Desktop\VpnProfileRadiusCert.cer"
```

<span data-ttu-id="c6d8e-109">Этот командлет используется для создания ZIP-файла профиля КЛИЕНТА VPN для ContosoVirtualNetworkGateway в ResourceGroup "ContosoResourceGroup".</span><span class="sxs-lookup"><span data-stu-id="c6d8e-109">This cmdlet is used to create a VPN client profile zip file for "ContosoVirtualNetworkGateway" in ResourceGroup "ContosoResourceGroup".</span></span> <span data-ttu-id="c6d8e-110">Профиль создается для предварительно настроенного сервера радиуса, для который настроен метод проверки подлинности EAPTLS с файлом сертификата VpnProfileRadiusCert.</span><span class="sxs-lookup"><span data-stu-id="c6d8e-110">The profile is generated for a pre-configured radius server that is configured to use "EAPTLS" authentication method with the VpnProfileRadiusCert certificate file.</span></span>

## <span data-ttu-id="c6d8e-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c6d8e-111">PARAMETERS</span></span>

### <span data-ttu-id="c6d8e-112">-AuthenticationMethod</span><span class="sxs-lookup"><span data-stu-id="c6d8e-112">-AuthenticationMethod</span></span>
<span data-ttu-id="c6d8e-113">Метод проверки подлинности может принимать значения EAPMSCHAPv2 или EAPTLS.</span><span class="sxs-lookup"><span data-stu-id="c6d8e-113">Authentication Method Can take values EAPMSCHAPv2 or EAPTLS.</span></span> <span data-ttu-id="c6d8e-114">Если задан протокол EAPMSCHAPv2, с помощью EAP-MSCHAPv2 протокола проверки подлинности создается установщик конфигурации клиента.</span><span class="sxs-lookup"><span data-stu-id="c6d8e-114">When EAPMSCHAPv2 is specified then the cmdlet generates a client configuration installer for username/password authentication that uses EAP-MSCHAPv2 authentication protocol.</span></span> <span data-ttu-id="c6d8e-115">Если задан протокол EAPTLS, для проверки подлинности сертификата с использованием протокола EAP-TLS создается установщик конфигурации клиента.</span><span class="sxs-lookup"><span data-stu-id="c6d8e-115">If EAPTLS is specified then the cmdlet generates a client configuration installer for certificate authentication that uses EAP-TLS protocol.</span></span> <span data-ttu-id="c6d8e-116">Параметр EapTls можно использовать как для проверки подлинности сертификата на основе RADIUS, так и для проверки сертификации, выполняемой виртуальным сетевым шлюзом путем отправки надежного корневого шлюза.</span><span class="sxs-lookup"><span data-stu-id="c6d8e-116">The "EapTls" option can be used for both RADIUS-based certificate authentication and certification authentication performed by the Virtual Network Gateway by uploading the trusted root.</span></span> <span data-ttu-id="c6d8e-117">Он автоматически определяет, какие настройки настроены.</span><span class="sxs-lookup"><span data-stu-id="c6d8e-117">The cmdlet automatically detects what is configured.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: EAPTLS, EAPMSCHAPv2

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6d8e-118">-ClientRootCertificateFileList</span><span class="sxs-lookup"><span data-stu-id="c6d8e-118">-ClientRootCertificateFileList</span></span>
<span data-ttu-id="c6d8e-119">Список путей корневого сертификата клиента</span><span class="sxs-lookup"><span data-stu-id="c6d8e-119">A list of client root certificate paths</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6d8e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6d8e-120">-DefaultProfile</span></span>
<span data-ttu-id="c6d8e-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c6d8e-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c6d8e-122">-Name</span><span class="sxs-lookup"><span data-stu-id="c6d8e-122">-Name</span></span>
<span data-ttu-id="c6d8e-123">Имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="c6d8e-123">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6d8e-124">-ProcessorArchitecture</span><span class="sxs-lookup"><span data-stu-id="c6d8e-124">-ProcessorArchitecture</span></span>
<span data-ttu-id="c6d8e-125">ProcessorArchitecture</span><span class="sxs-lookup"><span data-stu-id="c6d8e-125">ProcessorArchitecture</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Amd64, X86

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6d8e-126">-RadiusRootCertificateFile</span><span class="sxs-lookup"><span data-stu-id="c6d8e-126">-RadiusRootCertificateFile</span></span>
<span data-ttu-id="c6d8e-127">Путь корневого сертификата сервера Radius Server.</span><span class="sxs-lookup"><span data-stu-id="c6d8e-127">Radius server root certificate path.</span></span> <span data-ttu-id="c6d8e-128">Это обязательный параметр, который должен быть указан при проверке подлинности EAP-TLS с проверкой подлинности RADIUS.</span><span class="sxs-lookup"><span data-stu-id="c6d8e-128">This is a mandatory parameter that has to be specified when EAP-TLS with RADIUS authentication is used.</span></span> <span data-ttu-id="c6d8e-129">Это полный путь к файлу CER, содержащего корневой сертификат RADIUS, который клиент использует для проверки сервера RADIUS во время проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="c6d8e-129">This is the full path name of .cer file containing the RADIUS root certificate that the client uses to validates the RADIUS server during authentication.</span></span>

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

### <span data-ttu-id="c6d8e-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6d8e-130">-ResourceGroupName</span></span>
<span data-ttu-id="c6d8e-131">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c6d8e-131">The resource group name.</span></span>

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

### <span data-ttu-id="c6d8e-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c6d8e-132">-Confirm</span></span>
<span data-ttu-id="c6d8e-133">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c6d8e-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6d8e-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6d8e-134">-WhatIf</span></span>
<span data-ttu-id="c6d8e-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c6d8e-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c6d8e-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="c6d8e-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c6d8e-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6d8e-137">CommonParameters</span></span>
<span data-ttu-id="c6d8e-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6d8e-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6d8e-139">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6d8e-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6d8e-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c6d8e-140">INPUTS</span></span>

### <span data-ttu-id="c6d8e-141">System.String</span><span class="sxs-lookup"><span data-stu-id="c6d8e-141">System.String</span></span>

### <span data-ttu-id="c6d8e-142">System.String[]</span><span class="sxs-lookup"><span data-stu-id="c6d8e-142">System.String[]</span></span>

## <span data-ttu-id="c6d8e-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c6d8e-143">OUTPUTS</span></span>

### <span data-ttu-id="c6d8e-144">Microsoft.Azure.Commands.Network.Models.PSVpnProfile</span><span class="sxs-lookup"><span data-stu-id="c6d8e-144">Microsoft.Azure.Commands.Network.Models.PSVpnProfile</span></span>

## <span data-ttu-id="c6d8e-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c6d8e-145">NOTES</span></span>

## <span data-ttu-id="c6d8e-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c6d8e-146">RELATED LINKS</span></span>

[<span data-ttu-id="c6d8e-147">Get-AzVpnClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="c6d8e-147">Get-AzVpnClientConfiguration</span></span>](./Get-AzVpnClientConfiguration.md)
