---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 4522E93F-6AC9-4A37-88B8-CCCCE15A5879
online version: ''
schema: 2.0.0
ms.openlocfilehash: fcfc41e06f6847612c275817560e8593b76f6bac
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075471"
---
# <span data-ttu-id="a55fd-101">Reset-AzureRemoteAppVpnSharedKey</span><span class="sxs-lookup"><span data-stu-id="a55fd-101">Reset-AzureRemoteAppVpnSharedKey</span></span>

## <span data-ttu-id="a55fd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a55fd-102">SYNOPSIS</span></span>
<span data-ttu-id="a55fd-103">Сброс общего ключа VPN RemoteApp из Azure.</span><span class="sxs-lookup"><span data-stu-id="a55fd-103">Resets the Azure RemoteApp VPN shared key.</span></span>

## <span data-ttu-id="a55fd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a55fd-104">SYNTAX</span></span>

```
Reset-AzureRemoteAppVpnSharedKey [-VNetName] <String> [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a55fd-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a55fd-105">DESCRIPTION</span></span>
<span data-ttu-id="a55fd-106">Командлет **Reset-AzureRemoteAppVpnSharedKey** сбрасывает общий ключ виртуальной частной сети RemoteApp в Azure (VPN).</span><span class="sxs-lookup"><span data-stu-id="a55fd-106">The **Reset-AzureRemoteAppVpnSharedKey** cmdlet resets the Azure RemoteApp virtual private network (VPN) shared key.</span></span>

## <span data-ttu-id="a55fd-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a55fd-107">EXAMPLES</span></span>

### <span data-ttu-id="a55fd-108">Пример 1: сброс общего ключа в виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="a55fd-108">Example 1: Reset the shared key on a virtual network</span></span>
```
PS C:\> Reset-AzureRemoteAppVpnSharedKey -VNetName "ContosoVNet"
```

<span data-ttu-id="a55fd-109">Эта команда сбрасывает общий ключ в виртуальной сети с именем ContosoVNet.</span><span class="sxs-lookup"><span data-stu-id="a55fd-109">This command resets the shared key on the virtual network named ContosoVNet.</span></span>
<span data-ttu-id="a55fd-110">VPN-подключение к локальной сети остается в сети, пока на устройстве VPN не будет настроен новый общий ключ.</span><span class="sxs-lookup"><span data-stu-id="a55fd-110">The VPN connection to the on-premises network remains offline until the new shared key is configured on the VPN device.</span></span>
<span data-ttu-id="a55fd-111">Чтобы настроить VPN-устройство, используйте командлет **Get-AzureRemoteAppVpnDeviceConfigScript** , чтобы получить правильный сценарий или файл конфигурации для устройства VPN, а затем загрузите этот сценарий или файл конфигурации на устройство VPN.</span><span class="sxs-lookup"><span data-stu-id="a55fd-111">To configure the VPN device, use the **Get-AzureRemoteAppVpnDeviceConfigScript** cmdlet to retrieve the correct script or configuration file for your VPN device, then load that script or configuration file onto the VPN device.</span></span>

## <span data-ttu-id="a55fd-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a55fd-112">PARAMETERS</span></span>

### <span data-ttu-id="a55fd-113">-Profile</span><span class="sxs-lookup"><span data-stu-id="a55fd-113">-Profile</span></span>
<span data-ttu-id="a55fd-114">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="a55fd-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a55fd-115">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a55fd-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a55fd-116">-VNetName</span><span class="sxs-lookup"><span data-stu-id="a55fd-116">-VNetName</span></span>
<span data-ttu-id="a55fd-117">Указывает имя виртуальной сети RemoteApp Azure.</span><span class="sxs-lookup"><span data-stu-id="a55fd-117">Specifies the name of the Azure RemoteApp virtual network.</span></span>

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

### <span data-ttu-id="a55fd-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a55fd-118">-Confirm</span></span>
<span data-ttu-id="a55fd-119">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a55fd-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a55fd-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a55fd-120">-WhatIf</span></span>
<span data-ttu-id="a55fd-121">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a55fd-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a55fd-122">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a55fd-122">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a55fd-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a55fd-123">CommonParameters</span></span>
<span data-ttu-id="a55fd-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a55fd-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a55fd-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a55fd-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a55fd-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a55fd-126">INPUTS</span></span>

## <span data-ttu-id="a55fd-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a55fd-127">OUTPUTS</span></span>

### <span data-ttu-id="a55fd-128">System. String</span><span class="sxs-lookup"><span data-stu-id="a55fd-128">System.String</span></span>

## <span data-ttu-id="a55fd-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="a55fd-129">NOTES</span></span>

## <span data-ttu-id="a55fd-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a55fd-130">RELATED LINKS</span></span>

[<span data-ttu-id="a55fd-131">Get-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="a55fd-131">Get-AzureRemoteAppVNet</span></span>](./Get-AzureRemoteAppVNet.md)

[<span data-ttu-id="a55fd-132">Get-AzureRemoteAppVpnDeviceConfigScript</span><span class="sxs-lookup"><span data-stu-id="a55fd-132">Get-AzureRemoteAppVpnDeviceConfigScript</span></span>](./Get-AzureRemoteAppVpnDeviceConfigScript.md)


