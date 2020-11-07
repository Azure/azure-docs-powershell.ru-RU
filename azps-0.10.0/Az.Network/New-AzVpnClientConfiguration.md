---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnclientconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzVpnClientConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzVpnClientConfiguration.md
ms.openlocfilehash: caad6363e49d3ac3fe4e591fba860251c0a1d3c0
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93909594"
---
# <span data-ttu-id="02419-101">New-AzVpnClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="02419-101">New-AzVpnClientConfiguration</span></span>

## <span data-ttu-id="02419-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="02419-102">SYNOPSIS</span></span>
<span data-ttu-id="02419-103">Эта команда позволяет пользователям создавать пакеты профилей VPN на основе предварительно настроенных параметров VPN на шлюзе VPN в дополнение к некоторым дополнительным параметрам, которые может потребоваться настроить пользователи, например некоторые корневые сертификаты.</span><span class="sxs-lookup"><span data-stu-id="02419-103">This command allows the users to create the Vpn profile package based on pre-configured vpn settings on the VPN gateway, in addition to some additional settings that users may need to configure, for e.g. some root certificates.</span></span>

## <span data-ttu-id="02419-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="02419-104">SYNTAX</span></span>

```
New-AzVpnClientConfiguration [-Name <String>] -ResourceGroupName <String>
 [-ProcessorArchitecture <String>] -AuthenticationMethod <String> [-RadiusRootCertificateFile <String>]
 [-ClientRootCertificateFileList <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02419-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="02419-105">DESCRIPTION</span></span>
<span data-ttu-id="02419-106">Это позволит пользователям создавать пакеты профилей VPN на основе предварительно настроенных параметров VPN на шлюзе VPN в дополнение к некоторым дополнительным параметрам, которые может потребоваться настроить пользователи, например, с некоторыми корневыми сертификатами.</span><span class="sxs-lookup"><span data-stu-id="02419-106">this allows the users to create the Vpn profile package based on pre-configured vpn settings on the VPN gateway, in addition to some additional settings that users may need to configure, for e.g. some root certificates.</span></span>

## <span data-ttu-id="02419-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="02419-107">EXAMPLES</span></span>

### <span data-ttu-id="02419-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="02419-108">Example 1</span></span>
```
PS C:\> New-AzVpnClientConfiguration -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup" -AuthenticationMethod "EAPTLS" -RadiusRootCert "C:\Users\Test\Desktop\VpnProfileRadiusCert.cer"
```

<span data-ttu-id="02419-109">Этот командлет используется для создания ZIP-файла профиля клиента VPN для "ContosoVirtualNetworkGateway" в ResourceGroup "ContosoResourceGroup".</span><span class="sxs-lookup"><span data-stu-id="02419-109">This cmdlet is used to create a VPN client profile zip file for "ContosoVirtualNetworkGateway" in ResourceGroup "ContosoResourceGroup".</span></span> <span data-ttu-id="02419-110">Профиль создается для предварительно настроенного сервера RADIUS, который настроен на использование метода проверки подлинности "EAPTLS" с файлом сертификата VpnProfileRadiusCert.</span><span class="sxs-lookup"><span data-stu-id="02419-110">The profile is generated for a pre-configured radius server that is configured to use "EAPTLS" authentication method with the VpnProfileRadiusCert certificate file.</span></span>

## <span data-ttu-id="02419-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="02419-111">PARAMETERS</span></span>

### <span data-ttu-id="02419-112">-AuthenticationMethod</span><span class="sxs-lookup"><span data-stu-id="02419-112">-AuthenticationMethod</span></span>
<span data-ttu-id="02419-113">Метод проверки подлинности может принимать значения EAPMSCHAPv2 или EAPTLS.</span><span class="sxs-lookup"><span data-stu-id="02419-113">Authentication Method Can take values EAPMSCHAPv2 or EAPTLS.</span></span> <span data-ttu-id="02419-114">Если указан EAPMSCHAPv2, командлет создает установщик конфигурации клиента для проверки подлинности имени пользователя и пароля, использующего протокол проверки подлинности EAP-MSCHAPv2.</span><span class="sxs-lookup"><span data-stu-id="02419-114">When EAPMSCHAPv2 is specified then the cmdlet generates a client configuration installer for username/password authentication that uses EAP-MSCHAPv2 authentication protocol.</span></span> <span data-ttu-id="02419-115">Если указан EAPTLS, командлет создает установщик конфигурации клиента для проверки подлинности сертификата, использующей протокол EAP-TLS.</span><span class="sxs-lookup"><span data-stu-id="02419-115">If EAPTLS is specified then the cmdlet generates a client configuration installer for certificate authentication that uses EAP-TLS protocol.</span></span> <span data-ttu-id="02419-116">Параметр "EapTls" можно использовать как для проверки подлинности сертификата на основе RADIUS, так и для проверки подлинности сертификации, выполненной виртуальным сетевым шлюзом, загрузя доверенный корневой каталог.</span><span class="sxs-lookup"><span data-stu-id="02419-116">The "EapTls" option can be used for both RADIUS-based certificate authentication and certification authentication performed by the Virtual Network Gateway by uploading the trusted root.</span></span> <span data-ttu-id="02419-117">Командлет автоматически определяет, что настроено.</span><span class="sxs-lookup"><span data-stu-id="02419-117">The cmdlet automatically detects what is configured.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: EAPTLS, EAPMSCHAPv2

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02419-118">-ClientRootCertificateFileList</span><span class="sxs-lookup"><span data-stu-id="02419-118">-ClientRootCertificateFileList</span></span>
<span data-ttu-id="02419-119">Список путей к корневому сертификату клиента</span><span class="sxs-lookup"><span data-stu-id="02419-119">A list of client root certificate paths</span></span>
```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02419-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02419-120">-DefaultProfile</span></span>
<span data-ttu-id="02419-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="02419-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02419-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="02419-122">-Name</span></span>
<span data-ttu-id="02419-123">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="02419-123">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02419-124">-ProcessorArchitecture</span><span class="sxs-lookup"><span data-stu-id="02419-124">-ProcessorArchitecture</span></span>
<span data-ttu-id="02419-125">ProcessorArchitecture</span><span class="sxs-lookup"><span data-stu-id="02419-125">ProcessorArchitecture</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Amd64, X86

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02419-126">-RadiusRootCertificateFile</span><span class="sxs-lookup"><span data-stu-id="02419-126">-RadiusRootCertificateFile</span></span>
<span data-ttu-id="02419-127">Путь корневого сертификата RADIUS-сервера.</span><span class="sxs-lookup"><span data-stu-id="02419-127">Radius server root certificate path.</span></span> <span data-ttu-id="02419-128">Это обязательный параметр, который должен быть указан при использовании EAP-TLS с проверкой подлинности RADIUS.</span><span class="sxs-lookup"><span data-stu-id="02419-128">This is a mandatory parameter that has to be specified when EAP-TLS with RADIUS authentication is used.</span></span> <span data-ttu-id="02419-129">Это полный путь CER-файла, содержащего корневой сертификат RADIUS, который используется клиентом для проверки RADIUS-сервера во время проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="02419-129">This is the full path name of .cer file containing the RADIUS root certificate that the client uses to validates the RADIUS server during authentication.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02419-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02419-130">-ResourceGroupName</span></span>
<span data-ttu-id="02419-131">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="02419-131">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02419-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="02419-132">-Confirm</span></span>
<span data-ttu-id="02419-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="02419-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02419-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02419-134">-WhatIf</span></span>
<span data-ttu-id="02419-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="02419-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="02419-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="02419-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02419-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02419-137">CommonParameters</span></span>
<span data-ttu-id="02419-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="02419-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02419-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02419-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02419-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="02419-140">INPUTS</span></span>

### <span data-ttu-id="02419-141">System. String</span><span class="sxs-lookup"><span data-stu-id="02419-141">System.String</span></span>
<span data-ttu-id="02419-142">System. Collections. Generic. List "1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="02419-142">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="02419-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="02419-143">OUTPUTS</span></span>

### <span data-ttu-id="02419-144">Microsoft. Azure. Commands. Network. Models. PSVpnProfile</span><span class="sxs-lookup"><span data-stu-id="02419-144">Microsoft.Azure.Commands.Network.Models.PSVpnProfile</span></span>

## <span data-ttu-id="02419-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="02419-145">NOTES</span></span>

## <span data-ttu-id="02419-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="02419-146">RELATED LINKS</span></span>

