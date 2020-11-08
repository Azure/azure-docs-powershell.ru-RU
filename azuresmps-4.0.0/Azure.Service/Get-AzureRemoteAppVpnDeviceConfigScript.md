---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: D0E8B2BD-D68F-477A-9D66-C27AB737960D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 59423aa3de5ae91abe82090054fac61f3901363c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075625"
---
# <span data-ttu-id="46d99-101">Get-AzureRemoteAppVpnDeviceConfigScript</span><span class="sxs-lookup"><span data-stu-id="46d99-101">Get-AzureRemoteAppVpnDeviceConfigScript</span></span>

## <span data-ttu-id="46d99-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="46d99-102">SYNOPSIS</span></span>
<span data-ttu-id="46d99-103">Извлекает сценарий конфигурации для VPN-устройства RemoteApp Azure.</span><span class="sxs-lookup"><span data-stu-id="46d99-103">Retrieves the configuration script for an Azure RemoteApp VPN device.</span></span>

## <span data-ttu-id="46d99-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="46d99-104">SYNTAX</span></span>

```
Get-AzureRemoteAppVpnDeviceConfigScript [-VNetName] <String> [-Vendor] <String> [-Platform] <String>
 [-OSFamily] <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="46d99-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="46d99-105">DESCRIPTION</span></span>
<span data-ttu-id="46d99-106">Командлет **Get-AzureRemoteAppVpnDeviceConfigScript** извлекает сценарий конфигурации для устройства виртуальной частной сети REMOTEAPP (VPN) Azure.</span><span class="sxs-lookup"><span data-stu-id="46d99-106">The **Get-AzureRemoteAppVpnDeviceConfigScript** cmdlet retrieves the configuration script for an Azure RemoteApp virtual private network (VPN) device.</span></span>

## <span data-ttu-id="46d99-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="46d99-107">EXAMPLES</span></span>

### <span data-ttu-id="46d99-108">Пример 1: получение сценария конфигурации для устройства VPN</span><span class="sxs-lookup"><span data-stu-id="46d99-108">Example 1: Get a configuration script for a VPN device</span></span>
```
PS C:\> Get-AzureRemoteAppVpnDeviceConfigScript -VNetName "ContosoVNet" -Vendor "Microsoft Corporation" -OSFamily "Windows Server 2012 R2"
```

<span data-ttu-id="46d99-109">Эта команда возвращает сценарий или файл конфигурации, который используется для настройки VPN-устройства для виртуальной сети с именем ContosoVNet.</span><span class="sxs-lookup"><span data-stu-id="46d99-109">This command returns the script or configuration file used to configure the VPN device for the virtual network named ContosoVNet.</span></span>
<span data-ttu-id="46d99-110">Этот сценарий или файл конфигурации необходимо запустить или загрузить на устройство VPN обычным способом для этого устройства.</span><span class="sxs-lookup"><span data-stu-id="46d99-110">This script or configuration file should be run or loaded onto the VPN device in the typical manner for that device.</span></span>
<span data-ttu-id="46d99-111">Обратитесь к поставщику устройства VPN, чтобы получить уникальные требования для каждого устройства.</span><span class="sxs-lookup"><span data-stu-id="46d99-111">Consult the VPN device vendor for the unique requirements for each device.</span></span>

## <span data-ttu-id="46d99-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="46d99-112">PARAMETERS</span></span>

### <span data-ttu-id="46d99-113">-OSFamily</span><span class="sxs-lookup"><span data-stu-id="46d99-113">-OSFamily</span></span>
<span data-ttu-id="46d99-114">Определяет семейство операционной системы (ОС), которое работает на платформе устройства.</span><span class="sxs-lookup"><span data-stu-id="46d99-114">Specifies the operating system (OS) family that runs on the device platform.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="46d99-115">-Platform</span><span class="sxs-lookup"><span data-stu-id="46d99-115">-Platform</span></span>
<span data-ttu-id="46d99-116">Указывает платформу устройства.</span><span class="sxs-lookup"><span data-stu-id="46d99-116">Specifies the device platform.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="46d99-117">-Profile</span><span class="sxs-lookup"><span data-stu-id="46d99-117">-Profile</span></span>
<span data-ttu-id="46d99-118">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="46d99-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="46d99-119">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="46d99-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46d99-120">-Vendor</span><span class="sxs-lookup"><span data-stu-id="46d99-120">-Vendor</span></span>
<span data-ttu-id="46d99-121">Поставщик устройства VPN.</span><span class="sxs-lookup"><span data-stu-id="46d99-121">Specifies the vendor of the VPN device.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="46d99-122">-VNetName</span><span class="sxs-lookup"><span data-stu-id="46d99-122">-VNetName</span></span>
<span data-ttu-id="46d99-123">Указывает имя виртуальной сети RemoteApp Azure.</span><span class="sxs-lookup"><span data-stu-id="46d99-123">Specifies the name of an Azure RemoteApp virtual network.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="46d99-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46d99-124">CommonParameters</span></span>
<span data-ttu-id="46d99-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="46d99-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46d99-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46d99-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46d99-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="46d99-127">INPUTS</span></span>

## <span data-ttu-id="46d99-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="46d99-128">OUTPUTS</span></span>

## <span data-ttu-id="46d99-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="46d99-129">NOTES</span></span>

## <span data-ttu-id="46d99-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="46d99-130">RELATED LINKS</span></span>

[<span data-ttu-id="46d99-131">Get-AzureRemoteAppVpnDevice</span><span class="sxs-lookup"><span data-stu-id="46d99-131">Get-AzureRemoteAppVpnDevice</span></span>](./Get-AzureRemoteAppVpnDevice.md)


