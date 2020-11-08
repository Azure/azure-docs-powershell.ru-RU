---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 3E6EF9B8-9709-4E59-A1E5-78CDA4EAAE1B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 88dcd2f4bad149396d58948d3d656defdf055104
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075490"
---
# <span data-ttu-id="ab8be-101">Remove-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="ab8be-101">Remove-AzureVNetGateway</span></span>

## <span data-ttu-id="ab8be-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ab8be-102">SYNOPSIS</span></span>
<span data-ttu-id="ab8be-103">Удаляет шлюз VPN.</span><span class="sxs-lookup"><span data-stu-id="ab8be-103">Deletes a VPN gateway.</span></span>

## <span data-ttu-id="ab8be-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ab8be-104">SYNTAX</span></span>

```
Remove-AzureVNetGateway -VNetName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="ab8be-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ab8be-105">DESCRIPTION</span></span>
<span data-ttu-id="ab8be-106">Командлет **Remove-AzureVNetGateway** удаляет существующий шлюз виртуальной частной сети (VPN) для виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="ab8be-106">The **Remove-AzureVNetGateway** cmdlet deletes an existing virtual private network (VPN) gateway for a virtual network.</span></span>

## <span data-ttu-id="ab8be-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ab8be-107">EXAMPLES</span></span>

### <span data-ttu-id="ab8be-108">Пример 1: Удаление шлюза виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="ab8be-108">Example 1: Remove a virtual network gateway</span></span>
```
PS C:\> Remove-AzureVNetGateway -VNetName "ContosoVN07"
```

<span data-ttu-id="ab8be-109">Эта команда удаляет шлюз виртуальной сети из виртуальной сети с именем ContosoVN07.</span><span class="sxs-lookup"><span data-stu-id="ab8be-109">This command removes the virtual network gateway from the virtual network named ContosoVN07.</span></span>

## <span data-ttu-id="ab8be-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ab8be-110">PARAMETERS</span></span>

### <span data-ttu-id="ab8be-111">-Profile</span><span class="sxs-lookup"><span data-stu-id="ab8be-111">-Profile</span></span>
<span data-ttu-id="ab8be-112">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="ab8be-112">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="ab8be-113">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ab8be-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ab8be-114">-VNetName</span><span class="sxs-lookup"><span data-stu-id="ab8be-114">-VNetName</span></span>
<span data-ttu-id="ab8be-115">Указывает виртуальную сеть, в которой этот командлет удаляет VPN-шлюз.</span><span class="sxs-lookup"><span data-stu-id="ab8be-115">Specifies the virtual network in which this cmdlet deletes the VPN gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab8be-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab8be-116">CommonParameters</span></span>
<span data-ttu-id="ab8be-117">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ab8be-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab8be-118">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab8be-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab8be-119">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ab8be-119">INPUTS</span></span>

## <span data-ttu-id="ab8be-120">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ab8be-120">OUTPUTS</span></span>

## <span data-ttu-id="ab8be-121">Пуск</span><span class="sxs-lookup"><span data-stu-id="ab8be-121">NOTES</span></span>

## <span data-ttu-id="ab8be-122">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ab8be-122">RELATED LINKS</span></span>

[<span data-ttu-id="ab8be-123">Get-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="ab8be-123">Get-AzureVNetGateway</span></span>](./Get-AzureVNetGateway.md)

[<span data-ttu-id="ab8be-124">New-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="ab8be-124">New-AzureVNetGateway</span></span>](./New-AzureVNetGateway.md)

[<span data-ttu-id="ab8be-125">Сброс — AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="ab8be-125">Reset-AzureVNetGateway</span></span>](./Reset-AzureVNetGateway.md)

[<span data-ttu-id="ab8be-126">Изменить размер — AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="ab8be-126">Resize-AzureVNetGateway</span></span>](./Resize-AzureVNetGateway.md)

[<span data-ttu-id="ab8be-127">Set-AzureVNetGatewayKey</span><span class="sxs-lookup"><span data-stu-id="ab8be-127">Set-AzureVNetGatewayKey</span></span>](./Set-AzureVNetGatewayKey.md)


