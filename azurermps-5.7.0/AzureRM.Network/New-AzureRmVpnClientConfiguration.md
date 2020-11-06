---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvpnclientconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnClientConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnClientConfiguration.md
ms.openlocfilehash: 07618d546ebdadfb3313e17b881a7afbe09d1ff2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566570"
---
# <span data-ttu-id="5e86d-101">New-AzureRmVpnClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="5e86d-101">New-AzureRmVpnClientConfiguration</span></span>

## <span data-ttu-id="5e86d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5e86d-102">SYNOPSIS</span></span>
<span data-ttu-id="5e86d-103">Эта команда позволяет пользователям создавать пакеты профилей VPN на основе предварительно настроенных параметров VPN на шлюзе VPN в дополнение к некоторым дополнительным параметрам, которые может потребоваться настроить пользователи, например некоторые корневые сертификаты.</span><span class="sxs-lookup"><span data-stu-id="5e86d-103">This command allows the users to create the Vpn profile package based on pre-configured vpn settings on the VPN gateway, in addition to some additional settings that users may need to configure, for e.g. some root certificates.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5e86d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5e86d-104">SYNTAX</span></span>

```
New-AzureRmVpnClientConfiguration [-Name <String>] -ResourceGroupName <String>
 [-ProcessorArchitecture <String>] -AuthenticationMethod <String> [-RadiusRootCertificateFile <String>]
 [-ClientRootCertificateFileList <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e86d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5e86d-105">DESCRIPTION</span></span>
<span data-ttu-id="5e86d-106">Это позволит пользователям создавать пакеты профилей VPN на основе предварительно настроенных параметров VPN на шлюзе VPN в дополнение к некоторым дополнительным параметрам, которые может потребоваться настроить пользователи, например, с некоторыми корневыми сертификатами.</span><span class="sxs-lookup"><span data-stu-id="5e86d-106">this allows the users to create the Vpn profile package based on pre-configured vpn settings on the VPN gateway, in addition to some additional settings that users may need to configure, for e.g. some root certificates.</span></span>

## <span data-ttu-id="5e86d-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5e86d-107">EXAMPLES</span></span>

### <span data-ttu-id="5e86d-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5e86d-108">Example 1</span></span>
```
PS C:\> New-AzureRmVpnClientConfiguration -ResourceGroupName "ContosoResourceGroup" -Name "ContosoVirtualNetworkGateway" -AuthenticationMethod "EAPTLS" -RadiusRootCertificateFile "C:\Users\Test\Desktop\VpnProfileRadiusCert.cer"
```

<span data-ttu-id="5e86d-109">Этот командлет используется для создания ZIP-файла профиля клиента VPN для "ContosoVirtualNetworkGateway" в ResourceGroup "ContosoResourceGroup".</span><span class="sxs-lookup"><span data-stu-id="5e86d-109">This cmdlet is used to create a VPN client profile zip file for "ContosoVirtualNetworkGateway" in ResourceGroup "ContosoResourceGroup".</span></span> <span data-ttu-id="5e86d-110">Профиль создается для предварительно настроенного сервера RADIUS, который настроен на использование метода проверки подлинности "EAPTLS" с файлом сертификата VpnProfileRadiusCert.</span><span class="sxs-lookup"><span data-stu-id="5e86d-110">The profile is generated for a pre-configured radius server that is configured to use "EAPTLS" authentication method with the VpnProfileRadiusCert certificate file.</span></span>

## <span data-ttu-id="5e86d-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5e86d-111">PARAMETERS</span></span>

### <span data-ttu-id="5e86d-112">-AuthenticationMethod</span><span class="sxs-lookup"><span data-stu-id="5e86d-112">-AuthenticationMethod</span></span>
<span data-ttu-id="5e86d-113">Метод проверки подлинности может принимать значения EAPMSCHAPv2 или EAPTLS.</span><span class="sxs-lookup"><span data-stu-id="5e86d-113">Authentication Method Can take values EAPMSCHAPv2 or EAPTLS.</span></span> <span data-ttu-id="5e86d-114">Если указан EAPMSCHAPv2, командлет создает установщик конфигурации клиента для проверки подлинности имени пользователя и пароля, использующего протокол проверки подлинности EAP-MSCHAPv2.</span><span class="sxs-lookup"><span data-stu-id="5e86d-114">When EAPMSCHAPv2 is specified then the cmdlet generates a client configuration installer for username/password authentication that uses EAP-MSCHAPv2 authentication protocol.</span></span> <span data-ttu-id="5e86d-115">Если указан EAPTLS, командлет создает установщик конфигурации клиента для проверки подлинности сертификата, использующей протокол EAP-TLS.</span><span class="sxs-lookup"><span data-stu-id="5e86d-115">If EAPTLS is specified then the cmdlet generates a client configuration installer for certificate authentication that uses EAP-TLS protocol.</span></span> <span data-ttu-id="5e86d-116">Параметр "EapTls" можно использовать как для проверки подлинности сертификата на основе RADIUS, так и для проверки подлинности сертификации, выполненной виртуальным сетевым шлюзом, загрузя доверенный корневой каталог.</span><span class="sxs-lookup"><span data-stu-id="5e86d-116">The "EapTls" option can be used for both RADIUS-based certificate authentication and certification authentication performed by the Virtual Network Gateway by uploading the trusted root.</span></span> <span data-ttu-id="5e86d-117">Командлет автоматически определяет, что настроено.</span><span class="sxs-lookup"><span data-stu-id="5e86d-117">The cmdlet automatically detects what is configured.</span></span>

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

### <span data-ttu-id="5e86d-118">-ClientRootCertificateFileList</span><span class="sxs-lookup"><span data-stu-id="5e86d-118">-ClientRootCertificateFileList</span></span>
<span data-ttu-id="5e86d-119">Список путей к корневому сертификату клиента</span><span class="sxs-lookup"><span data-stu-id="5e86d-119">A list of client root certificate paths</span></span>
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

### <span data-ttu-id="5e86d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e86d-120">-DefaultProfile</span></span>
<span data-ttu-id="5e86d-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5e86d-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
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

### <span data-ttu-id="5e86d-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5e86d-122">-Name</span></span>
<span data-ttu-id="5e86d-123">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="5e86d-123">The resource name.</span></span>

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

### <span data-ttu-id="5e86d-124">-ProcessorArchitecture</span><span class="sxs-lookup"><span data-stu-id="5e86d-124">-ProcessorArchitecture</span></span>
<span data-ttu-id="5e86d-125">ProcessorArchitecture</span><span class="sxs-lookup"><span data-stu-id="5e86d-125">ProcessorArchitecture</span></span>

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

### <span data-ttu-id="5e86d-126">-RadiusRootCertificateFile</span><span class="sxs-lookup"><span data-stu-id="5e86d-126">-RadiusRootCertificateFile</span></span>
<span data-ttu-id="5e86d-127">Путь корневого сертификата RADIUS-сервера.</span><span class="sxs-lookup"><span data-stu-id="5e86d-127">Radius server root certificate path.</span></span> <span data-ttu-id="5e86d-128">Это обязательный параметр, который должен быть указан при использовании EAP-TLS с проверкой подлинности RADIUS.</span><span class="sxs-lookup"><span data-stu-id="5e86d-128">This is a mandatory parameter that has to be specified when EAP-TLS with RADIUS authentication is used.</span></span> <span data-ttu-id="5e86d-129">Это полный путь CER-файла, содержащего корневой сертификат RADIUS, который используется клиентом для проверки RADIUS-сервера во время проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="5e86d-129">This is the full path name of .cer file containing the RADIUS root certificate that the client uses to validates the RADIUS server during authentication.</span></span>

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

### <span data-ttu-id="5e86d-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e86d-130">-ResourceGroupName</span></span>
<span data-ttu-id="5e86d-131">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5e86d-131">The resource group name.</span></span>

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

### <span data-ttu-id="5e86d-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5e86d-132">-Confirm</span></span>
<span data-ttu-id="5e86d-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5e86d-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e86d-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e86d-134">-WhatIf</span></span>
<span data-ttu-id="5e86d-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5e86d-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5e86d-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5e86d-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e86d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e86d-137">CommonParameters</span></span>
<span data-ttu-id="5e86d-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5e86d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e86d-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e86d-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e86d-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5e86d-140">INPUTS</span></span>

### <span data-ttu-id="5e86d-141">System. String</span><span class="sxs-lookup"><span data-stu-id="5e86d-141">System.String</span></span>
<span data-ttu-id="5e86d-142">System. Collections. Generic. List "1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="5e86d-142">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="5e86d-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5e86d-143">OUTPUTS</span></span>

### <span data-ttu-id="5e86d-144">Microsoft. Azure. Commands. Network. Models. PSVpnProfile</span><span class="sxs-lookup"><span data-stu-id="5e86d-144">Microsoft.Azure.Commands.Network.Models.PSVpnProfile</span></span>

## <span data-ttu-id="5e86d-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="5e86d-145">NOTES</span></span>

## <span data-ttu-id="5e86d-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5e86d-146">RELATED LINKS</span></span>

