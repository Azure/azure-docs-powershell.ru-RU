---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2B4A3E2A-1868-492F-9F77-932319D2CE6D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnclientpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientPackage.md
ms.openlocfilehash: ec91fecd41138238bc4d89fa81d77bae4730c770
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100399402"
---
# <span data-ttu-id="be023-101">Get-AzVpnClientPackage</span><span class="sxs-lookup"><span data-stu-id="be023-101">Get-AzVpnClientPackage</span></span>

## <span data-ttu-id="be023-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="be023-102">SYNOPSIS</span></span>
<span data-ttu-id="be023-103">Сведения о пакете клиента VPN.</span><span class="sxs-lookup"><span data-stu-id="be023-103">Gets information about a VPN client package.</span></span>

## <span data-ttu-id="be023-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="be023-104">SYNTAX</span></span>

```
Get-AzVpnClientPackage -ResourceGroupName <String> -VirtualNetworkGatewayName <String>
 -ProcessorArchitecture <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="be023-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="be023-105">DESCRIPTION</span></span>
<span data-ttu-id="be023-106">С **помощью cmdlet get-AzVpnClientPackage** можно получить сведения о пакетах клиента VPN, которые доступны для виртуального сетевого шлюза.</span><span class="sxs-lookup"><span data-stu-id="be023-106">The **Get-AzVpnClientPackage** cmdlet gets information about the VPN client packages available from a virtual network gateway.</span></span>
<span data-ttu-id="be023-107">Пакеты клиента содержат данные конфигурации, позволяющие клиентский компьютеру использовать VPN-подключение к виртуальной сети Azure; Чтобы установить VPN-подключение, на клиентских компьютерах должен быть установлен правильный пакет конфигурации.</span><span class="sxs-lookup"><span data-stu-id="be023-107">Client packages contain configuration data that enable a client computer to make a VPN connection to an Azure virtual network; client computers must have the correct configuration package installed in order to make a VPN connection.</span></span>
<span data-ttu-id="be023-108">Доступные пакеты конфигурации основаны на версии Windows клиентского компьютера (например, Windows 7 или Windows 10) и архитектуре процессора клиентского компьютера (AMD64 или x86).</span><span class="sxs-lookup"><span data-stu-id="be023-108">Different configuration packages are available based on the client computer's version of Windows (for example, Windows 7 or Windows 10) and on the client computer's processor architecture (AMD64 or x86).</span></span>
<span data-ttu-id="be023-109">Тип архитектуры необходимо указать при запуске **Get-AzVpnClientPackage.**</span><span class="sxs-lookup"><span data-stu-id="be023-109">You must specify the architecture type when running **Get-AzVpnClientPackage**.</span></span>

## <span data-ttu-id="be023-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="be023-110">EXAMPLES</span></span>

### <span data-ttu-id="be023-111">Пример 1. Сведения о пакете клиента VPN для процессоров</span><span class="sxs-lookup"><span data-stu-id="be023-111">Example 1: Get information about a processor architecture VPN client package</span></span>
```
PS C:\>Get-AzVpnClientPackage -ProcessorArchitecture -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup" -ProcessorArchitecture "Amd64"
```

<span data-ttu-id="be023-112">Эта команда получает сведения о пакетах клиента AMD64 VPN, которые хранятся в виртуальном сетевом шлюзе ContosoVirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="be023-112">This command gets information about the AMD64 VPN client packages stored on the virtual network gateway named ContosoVirtualNetworkGateway.</span></span>
<span data-ttu-id="be023-113">Чтобы получить сведения о пакетах клиента x86, установите для параметра *ProcessorArchitecture* значение x86.</span><span class="sxs-lookup"><span data-stu-id="be023-113">To get information about the x86 client packages, set the value of the *ProcessorArchitecture* parameter to x86.</span></span>

## <span data-ttu-id="be023-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="be023-114">PARAMETERS</span></span>

### <span data-ttu-id="be023-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be023-115">-DefaultProfile</span></span>
<span data-ttu-id="be023-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="be023-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="be023-117">-ProcessorArchitecture</span><span class="sxs-lookup"><span data-stu-id="be023-117">-ProcessorArchitecture</span></span>
<span data-ttu-id="be023-118">Определяет тип архитектуры ЦП, для которую предназначен пакет клиента.</span><span class="sxs-lookup"><span data-stu-id="be023-118">Specifies the type of CPU architecture that the client package is designed for.</span></span>
<span data-ttu-id="be023-119">Допустимые значения: Amd64 и X86.</span><span class="sxs-lookup"><span data-stu-id="be023-119">Valid values are Amd64 and X86.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Amd64, X86

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be023-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be023-120">-ResourceGroupName</span></span>
<span data-ttu-id="be023-121">Указывает имя группы ресурсов, которая назначена виртуальному сетевому шлюзу.</span><span class="sxs-lookup"><span data-stu-id="be023-121">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>
<span data-ttu-id="be023-122">Группы ресурсов группируют элементы, чтобы упростить управление запасами и общее администрирование Azure.</span><span class="sxs-lookup"><span data-stu-id="be023-122">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="be023-123">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="be023-123">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="be023-124">Указывает имя виртуального сетевого шлюза, в котором хранится информация о пакете клиента.</span><span class="sxs-lookup"><span data-stu-id="be023-124">Specifies the name of the virtual network gateway where the client package information is stored.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="be023-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be023-125">CommonParameters</span></span>
<span data-ttu-id="be023-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be023-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be023-127">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="be023-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be023-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="be023-128">INPUTS</span></span>

### <span data-ttu-id="be023-129">System.String</span><span class="sxs-lookup"><span data-stu-id="be023-129">System.String</span></span>

## <span data-ttu-id="be023-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="be023-130">OUTPUTS</span></span>

### <span data-ttu-id="be023-131">System.String</span><span class="sxs-lookup"><span data-stu-id="be023-131">System.String</span></span>

## <span data-ttu-id="be023-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="be023-132">NOTES</span></span>

## <span data-ttu-id="be023-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="be023-133">RELATED LINKS</span></span>

[<span data-ttu-id="be023-134">Resize-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="be023-134">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)



