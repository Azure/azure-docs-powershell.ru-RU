---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 7B749B29-9820-4E23-B5AF-F5535251629A
online version: ''
schema: 2.0.0
ms.openlocfilehash: ec94df29fb23dd7c82d79304c2e48aab225ed224
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076287"
---
# <span data-ttu-id="10b46-101">Get-AzureVNetConnection</span><span class="sxs-lookup"><span data-stu-id="10b46-101">Get-AzureVNetConnection</span></span>

## <span data-ttu-id="10b46-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="10b46-102">SYNOPSIS</span></span>
<span data-ttu-id="10b46-103">Получение подключений к виртуальной сети Azure.</span><span class="sxs-lookup"><span data-stu-id="10b46-103">Gets connections to an Azure virtual network.</span></span>

## <span data-ttu-id="10b46-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="10b46-104">SYNTAX</span></span>

```
Get-AzureVNetConnection -VNetName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="10b46-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="10b46-105">DESCRIPTION</span></span>
<span data-ttu-id="10b46-106">Командлет **Get-AzureVNetConnection** возвращает объект, указывающий все активные подключения к виртуальной частной сети (VPN) в виртуальную сеть Azure.</span><span class="sxs-lookup"><span data-stu-id="10b46-106">The **Get-AzureVNetConnection** cmdlet returns an object that specifies all active virtual private network (VPN) connections to an Azure virtual network.</span></span>
<span data-ttu-id="10b46-107">VPN-подключения включают в себя виртуальные сети VPN между сайтами и виртуальную сеть.</span><span class="sxs-lookup"><span data-stu-id="10b46-107">VPN connections include cross premises site-to-site VPNs and virtual network to virtual network connections.</span></span>

## <span data-ttu-id="10b46-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="10b46-108">EXAMPLES</span></span>

## <span data-ttu-id="10b46-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="10b46-109">PARAMETERS</span></span>

### <span data-ttu-id="10b46-110">-Profile</span><span class="sxs-lookup"><span data-stu-id="10b46-110">-Profile</span></span>
<span data-ttu-id="10b46-111">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="10b46-111">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="10b46-112">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="10b46-112">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="10b46-113">-VNetName</span><span class="sxs-lookup"><span data-stu-id="10b46-113">-VNetName</span></span>
<span data-ttu-id="10b46-114">Указывает имя виртуальной сети, из которой этот командлет возвращает подключения.</span><span class="sxs-lookup"><span data-stu-id="10b46-114">Specifies the name of the virtual network from which this cmdlet returns connections.</span></span>

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

### <span data-ttu-id="10b46-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10b46-115">CommonParameters</span></span>
<span data-ttu-id="10b46-116">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="10b46-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10b46-117">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10b46-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10b46-118">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="10b46-118">INPUTS</span></span>

## <span data-ttu-id="10b46-119">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="10b46-119">OUTPUTS</span></span>

## <span data-ttu-id="10b46-120">Пуск</span><span class="sxs-lookup"><span data-stu-id="10b46-120">NOTES</span></span>

## <span data-ttu-id="10b46-121">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="10b46-121">RELATED LINKS</span></span>

