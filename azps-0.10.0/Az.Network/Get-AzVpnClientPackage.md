---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2B4A3E2A-1868-492F-9F77-932319D2CE6D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnclientpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVpnClientPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVpnClientPackage.md
ms.openlocfilehash: d08f91029940d60440d50be406dbdfe3652934a7
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93909822"
---
# <span data-ttu-id="889e0-101">Get-AzVpnClientPackage</span><span class="sxs-lookup"><span data-stu-id="889e0-101">Get-AzVpnClientPackage</span></span>

## <span data-ttu-id="889e0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="889e0-102">SYNOPSIS</span></span>
<span data-ttu-id="889e0-103">Получение сведений о пакете VPN-клиента.</span><span class="sxs-lookup"><span data-stu-id="889e0-103">Gets information about a VPN client package.</span></span>

## <span data-ttu-id="889e0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="889e0-104">SYNTAX</span></span>

```
Get-AzVpnClientPackage -ResourceGroupName <String> -VirtualNetworkGatewayName <String>
 -ProcessorArchitecture <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="889e0-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="889e0-105">DESCRIPTION</span></span>
<span data-ttu-id="889e0-106">Командлет **Get-AzVpnClientPackage** получает сведения о ПАКЕТах VPN-клиентов, доступных на шлюзе виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="889e0-106">The **Get-AzVpnClientPackage** cmdlet gets information about the VPN client packages available from a virtual network gateway.</span></span>
<span data-ttu-id="889e0-107">Пакеты клиентов содержат данные конфигурации, позволяющие клиентскому компьютеру выполнять VPN-подключение к виртуальной сети Azure; для создания VPN-подключения клиентские компьютеры должны установить правильный пакет конфигурации.</span><span class="sxs-lookup"><span data-stu-id="889e0-107">Client packages contain configuration data that enable a client computer to make a VPN connection to an Azure virtual network; client computers must have the correct configuration package installed in order to make a VPN connection.</span></span>
<span data-ttu-id="889e0-108">Различные пакеты конфигурации доступны в зависимости от версии Windows на клиентском компьютере (например, Windows 7 или Windows 10) и архитектуры процессора на клиентском компьютере (AMD64 или x86).</span><span class="sxs-lookup"><span data-stu-id="889e0-108">Different configuration packages are available based on the client computer's version of Windows (for example, Windows 7 or Windows 10) and on the client computer's processor architecture (AMD64 or x86).</span></span>
<span data-ttu-id="889e0-109">При запуске **Get-AzVpnClientPackage** необходимо указать тип архитектуры.</span><span class="sxs-lookup"><span data-stu-id="889e0-109">You must specify the architecture type when running **Get-AzVpnClientPackage**.</span></span>

## <span data-ttu-id="889e0-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="889e0-110">EXAMPLES</span></span>

### <span data-ttu-id="889e0-111">Пример 1: получение сведений о пакете клиента для архитектуры процессора VPN</span><span class="sxs-lookup"><span data-stu-id="889e0-111">Example 1: Get information about a processor architecture VPN client package</span></span>
```
PS C:\>Get-AzVpnClientPackage -ProcessorArchitecture -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup" -ProcessorArchitecture "Amd64"
```

<span data-ttu-id="889e0-112">Эта команда получает сведения о пакетах VPN-клиентов AMD64, хранящихся на виртуальном сетевом шлюзе с именем ContosoVirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="889e0-112">This command gets information about the AMD64 VPN client packages stored on the virtual network gateway named ContosoVirtualNetworkGateway.</span></span>
<span data-ttu-id="889e0-113">Чтобы получить сведения о пакетах клиентов x86, установите для параметра *processorArchitecture* значение x86.</span><span class="sxs-lookup"><span data-stu-id="889e0-113">To get information about the x86 client packages, set the value of the *ProcessorArchitecture* parameter to x86.</span></span>

## <span data-ttu-id="889e0-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="889e0-114">PARAMETERS</span></span>

### <span data-ttu-id="889e0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="889e0-115">-DefaultProfile</span></span>
<span data-ttu-id="889e0-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="889e0-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="889e0-117">-ProcessorArchitecture</span><span class="sxs-lookup"><span data-stu-id="889e0-117">-ProcessorArchitecture</span></span>
<span data-ttu-id="889e0-118">Указывает тип архитектуры ЦП, для которой предназначен клиентский пакет.</span><span class="sxs-lookup"><span data-stu-id="889e0-118">Specifies the type of CPU architecture that the client package is designed for.</span></span>
<span data-ttu-id="889e0-119">Допустимые значения: AMD64 и x86.</span><span class="sxs-lookup"><span data-stu-id="889e0-119">Valid values are Amd64 and X86.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Amd64, X86

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="889e0-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="889e0-120">-ResourceGroupName</span></span>
<span data-ttu-id="889e0-121">Указывает имя группы ресурсов, которой назначен шлюз виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="889e0-121">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>

<span data-ttu-id="889e0-122">Группы ресурсов классифицируют элементы для облегчения управления запасами и общего администрирования Azure.</span><span class="sxs-lookup"><span data-stu-id="889e0-122">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="889e0-123">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="889e0-123">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="889e0-124">Указывает имя шлюза виртуальной сети, в котором хранятся сведения о клиентском пакете.</span><span class="sxs-lookup"><span data-stu-id="889e0-124">Specifies the name of the virtual network gateway where the client package information is stored.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="889e0-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="889e0-125">CommonParameters</span></span>
<span data-ttu-id="889e0-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="889e0-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="889e0-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="889e0-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="889e0-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="889e0-128">INPUTS</span></span>

### <span data-ttu-id="889e0-129">Подстрок</span><span class="sxs-lookup"><span data-stu-id="889e0-129">String</span></span>
<span data-ttu-id="889e0-130">Параметр "ResourceGroupName" принимает значение типа String из конвейера.</span><span class="sxs-lookup"><span data-stu-id="889e0-130">Parameter 'ResourceGroupName' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="889e0-131">Подстрок</span><span class="sxs-lookup"><span data-stu-id="889e0-131">String</span></span>
<span data-ttu-id="889e0-132">Параметр "VirtualNetworkGatewayName" принимает значение типа String из конвейера.</span><span class="sxs-lookup"><span data-stu-id="889e0-132">Parameter 'VirtualNetworkGatewayName' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="889e0-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="889e0-133">OUTPUTS</span></span>

###  
<span data-ttu-id="889e0-134">Функция **Get-AzVpnClientPackage** возвращает экземпляры объекта System. String.</span><span class="sxs-lookup"><span data-stu-id="889e0-134">**Get-AzVpnClientPackage** returns instances of the System.String object.</span></span>

## <span data-ttu-id="889e0-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="889e0-135">NOTES</span></span>

## <span data-ttu-id="889e0-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="889e0-136">RELATED LINKS</span></span>

[<span data-ttu-id="889e0-137">Изменить размер — AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="889e0-137">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)

[<span data-ttu-id="889e0-138">Set-AzVirtualNetworkGatewayVpnClientConfig</span><span class="sxs-lookup"><span data-stu-id="889e0-138">Set-AzVirtualNetworkGatewayVpnClientConfig</span></span>](./Set-AzVirtualNetworkGatewayVpnClientConfig.md)


