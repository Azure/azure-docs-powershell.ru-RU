---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvpnclientconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientConfiguration.md
ms.openlocfilehash: e5dd9da25bfa2c27bd605dc80b04f8e47fb7f95b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101964120"
---
# <span data-ttu-id="9247b-101">New-AzVpnClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="9247b-101">New-AzVpnClientConfiguration</span></span>

## <span data-ttu-id="9247b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9247b-102">SYNOPSIS</span></span>
<span data-ttu-id="9247b-103">Эта команда позволяет пользователям создавать пакет профиля VPN на основе предварительно настроенных параметров VPN-шлюза, а также настраивать некоторые дополнительные параметры, например некоторые корневые сертификаты.</span><span class="sxs-lookup"><span data-stu-id="9247b-103">This command allows the users to create the Vpn profile package based on pre-configured vpn settings on the VPN gateway, in addition to some additional settings that users may need to configure, for e.g. some root certificates.</span></span>

## <span data-ttu-id="9247b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9247b-104">SYNTAX</span></span>

```
New-AzVpnClientConfiguration [-Name <String>] -ResourceGroupName <String> [-ProcessorArchitecture <String>]
 [-AuthenticationMethod <String>] [-RadiusRootCertificateFile <String>]
 [-ClientRootCertificateFileList <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9247b-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9247b-105">DESCRIPTION</span></span>
<span data-ttu-id="9247b-106">это позволит пользователям создавать пакет профиля VPN на основе предварительно настроенных параметров VPN на шлюзе VPN, а также настраивать некоторые дополнительные параметры, например некоторые корневые сертификаты.</span><span class="sxs-lookup"><span data-stu-id="9247b-106">this allows the users to create the Vpn profile package based on pre-configured vpn settings on the VPN gateway, in addition to some additional settings that users may need to configure, for e.g. some root certificates.</span></span>

## <span data-ttu-id="9247b-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9247b-107">EXAMPLES</span></span>

### <span data-ttu-id="9247b-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9247b-108">Example 1</span></span>
```
PS C:\> New-AzVpnClientConfiguration -ResourceGroupName "ContosoResourceGroup" -Name "ContosoVirtualNetworkGateway" -AuthenticationMethod "EAPTLS" -RadiusRootCertificateFile "C:\Users\Test\Desktop\VpnProfileRadiusCert.cer"
```

<span data-ttu-id="9247b-109">Этот командлет используется для создания ZIP-файла профиля КЛИЕНТА VPN для ContosoVirtualNetworkGateway в ResourceGroup "ContosoResourceGroup".</span><span class="sxs-lookup"><span data-stu-id="9247b-109">This cmdlet is used to create a VPN client profile zip file for "ContosoVirtualNetworkGateway" in ResourceGroup "ContosoResourceGroup".</span></span> <span data-ttu-id="9247b-110">Профиль создается для предварительно настроенного сервера радиуса, для который настроен метод проверки подлинности EAPTLS с файлом сертификата VpnProfileRadiusCert.</span><span class="sxs-lookup"><span data-stu-id="9247b-110">The profile is generated for a pre-configured radius server that is configured to use "EAPTLS" authentication method with the VpnProfileRadiusCert certificate file.</span></span>

## <span data-ttu-id="9247b-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9247b-111">PARAMETERS</span></span>

### <span data-ttu-id="9247b-112">-AuthenticationMethod</span><span class="sxs-lookup"><span data-stu-id="9247b-112">-AuthenticationMethod</span></span>
<span data-ttu-id="9247b-113">Метод проверки подлинности может принимать значения EAPMSCHAPv2 или EAPTLS.</span><span class="sxs-lookup"><span data-stu-id="9247b-113">Authentication Method Can take values EAPMSCHAPv2 or EAPTLS.</span></span> <span data-ttu-id="9247b-114">Если задан протокол EAPMSCHAPv2, с помощью EAP-MSCHAPv2 протокола проверки подлинности создается установщик конфигурации клиента.</span><span class="sxs-lookup"><span data-stu-id="9247b-114">When EAPMSCHAPv2 is specified then the cmdlet generates a client configuration installer for username/password authentication that uses EAP-MSCHAPv2 authentication protocol.</span></span> <span data-ttu-id="9247b-115">Если задан протокол EAPTLS, для проверки подлинности сертификата с использованием протокола EAP-TLS создается установщик конфигурации клиента.</span><span class="sxs-lookup"><span data-stu-id="9247b-115">If EAPTLS is specified then the cmdlet generates a client configuration installer for certificate authentication that uses EAP-TLS protocol.</span></span> <span data-ttu-id="9247b-116">Параметр EapTls можно использовать как для проверки подлинности сертификата на основе RADIUS, так и для проверки сертификации, выполняемой виртуальным сетевым шлюзом путем отправки надежного корневого шлюза.</span><span class="sxs-lookup"><span data-stu-id="9247b-116">The "EapTls" option can be used for both RADIUS-based certificate authentication and certification authentication performed by the Virtual Network Gateway by uploading the trusted root.</span></span> <span data-ttu-id="9247b-117">Он автоматически определяет, какие настройки настроены.</span><span class="sxs-lookup"><span data-stu-id="9247b-117">The cmdlet automatically detects what is configured.</span></span>

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

### <span data-ttu-id="9247b-118">-ClientRootCertificateFileList</span><span class="sxs-lookup"><span data-stu-id="9247b-118">-ClientRootCertificateFileList</span></span>
<span data-ttu-id="9247b-119">Список путей корневого сертификата клиента</span><span class="sxs-lookup"><span data-stu-id="9247b-119">A list of client root certificate paths</span></span>

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

### <span data-ttu-id="9247b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9247b-120">-DefaultProfile</span></span>
<span data-ttu-id="9247b-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9247b-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9247b-122">-Name</span><span class="sxs-lookup"><span data-stu-id="9247b-122">-Name</span></span>
<span data-ttu-id="9247b-123">Имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="9247b-123">The resource name.</span></span>

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

### <span data-ttu-id="9247b-124">-ProcessorArchitecture</span><span class="sxs-lookup"><span data-stu-id="9247b-124">-ProcessorArchitecture</span></span>
<span data-ttu-id="9247b-125">ProcessorArchitecture</span><span class="sxs-lookup"><span data-stu-id="9247b-125">ProcessorArchitecture</span></span>

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

### <span data-ttu-id="9247b-126">-RadiusRootCertificateFile</span><span class="sxs-lookup"><span data-stu-id="9247b-126">-RadiusRootCertificateFile</span></span>
<span data-ttu-id="9247b-127">Путь корневого сертификата сервера Radius Server.</span><span class="sxs-lookup"><span data-stu-id="9247b-127">Radius server root certificate path.</span></span> <span data-ttu-id="9247b-128">Это обязательный параметр, который должен быть указан при проверке подлинности EAP-TLS с проверкой подлинности RADIUS.</span><span class="sxs-lookup"><span data-stu-id="9247b-128">This is a mandatory parameter that has to be specified when EAP-TLS with RADIUS authentication is used.</span></span> <span data-ttu-id="9247b-129">Это полный путь к файлу CER, содержащего корневой сертификат RADIUS, который клиент использует для проверки сервера RADIUS во время проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="9247b-129">This is the full path name of .cer file containing the RADIUS root certificate that the client uses to validates the RADIUS server during authentication.</span></span>

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

### <span data-ttu-id="9247b-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9247b-130">-ResourceGroupName</span></span>
<span data-ttu-id="9247b-131">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9247b-131">The resource group name.</span></span>

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

### <span data-ttu-id="9247b-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9247b-132">-Confirm</span></span>
<span data-ttu-id="9247b-133">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9247b-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9247b-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9247b-134">-WhatIf</span></span>
<span data-ttu-id="9247b-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9247b-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9247b-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="9247b-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9247b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9247b-137">CommonParameters</span></span>
<span data-ttu-id="9247b-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9247b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9247b-139">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9247b-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9247b-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9247b-140">INPUTS</span></span>

### <span data-ttu-id="9247b-141">System.String</span><span class="sxs-lookup"><span data-stu-id="9247b-141">System.String</span></span>

### <span data-ttu-id="9247b-142">System.String[]</span><span class="sxs-lookup"><span data-stu-id="9247b-142">System.String[]</span></span>

## <span data-ttu-id="9247b-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9247b-143">OUTPUTS</span></span>

### <span data-ttu-id="9247b-144">Microsoft.Azure.Commands.Network.Models.PSVpnProfile</span><span class="sxs-lookup"><span data-stu-id="9247b-144">Microsoft.Azure.Commands.Network.Models.PSVpnProfile</span></span>

## <span data-ttu-id="9247b-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9247b-145">NOTES</span></span>

## <span data-ttu-id="9247b-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9247b-146">RELATED LINKS</span></span>

[<span data-ttu-id="9247b-147">Get-AzVpnClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="9247b-147">Get-AzVpnClientConfiguration</span></span>](./Get-AzVpnClientConfiguration.md)
