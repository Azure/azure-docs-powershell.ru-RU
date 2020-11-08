---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 4024D20D-46DF-4ED8-A091-E6E17F840E40
online version: ''
schema: 2.0.0
ms.openlocfilehash: 92c6ba8827906fbfc51b121e4500dea3ec4555d9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076279"
---
# <span data-ttu-id="d210a-101">Get-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="d210a-101">Get-AzureVNetGateway</span></span>

## <span data-ttu-id="d210a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d210a-102">SYNOPSIS</span></span>
<span data-ttu-id="d210a-103">Возвращает состояние шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="d210a-103">Gets the status of a virtual network gateway.</span></span>

## <span data-ttu-id="d210a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d210a-104">SYNTAX</span></span>

```
Get-AzureVNetGateway -VNetName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="d210a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d210a-105">DESCRIPTION</span></span>
<span data-ttu-id="d210a-106">Командлет **Get-AzureVNetGateway** получает состояние существующего шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="d210a-106">The **Get-AzureVNetGateway** cmdlet gets the status of an existing virtual network gateway.</span></span>

## <span data-ttu-id="d210a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d210a-107">EXAMPLES</span></span>

### <span data-ttu-id="d210a-108">Пример 1: получение состояния шлюза виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="d210a-108">Example 1: Get the status of a virtual network gateway</span></span>
```
PS C:\> Get-AzureVNetGateway -VNetName "ContosoVN07"
```

<span data-ttu-id="d210a-109">Эта команда получает состояние шлюза виртуальной сети для виртуальной сети с именем ContosoVN07.</span><span class="sxs-lookup"><span data-stu-id="d210a-109">This command gets that status of the virtual network gateway for the virtual network named ContosoVN07.</span></span>

## <span data-ttu-id="d210a-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d210a-110">PARAMETERS</span></span>

### <span data-ttu-id="d210a-111">-Profile</span><span class="sxs-lookup"><span data-stu-id="d210a-111">-Profile</span></span>
<span data-ttu-id="d210a-112">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="d210a-112">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="d210a-113">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d210a-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d210a-114">-VNetName</span><span class="sxs-lookup"><span data-stu-id="d210a-114">-VNetName</span></span>
<span data-ttu-id="d210a-115">Указывает виртуальную сеть, которая содержит шлюз виртуальной сети, которому этот командлет получает состояние.</span><span class="sxs-lookup"><span data-stu-id="d210a-115">Specifies the virtual network that contains the virtual network gateway for which this cmdlet gets status.</span></span>

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

### <span data-ttu-id="d210a-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d210a-116">CommonParameters</span></span>
<span data-ttu-id="d210a-117">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d210a-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d210a-118">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d210a-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d210a-119">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d210a-119">INPUTS</span></span>

## <span data-ttu-id="d210a-120">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d210a-120">OUTPUTS</span></span>

## <span data-ttu-id="d210a-121">Пуск</span><span class="sxs-lookup"><span data-stu-id="d210a-121">NOTES</span></span>

## <span data-ttu-id="d210a-122">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d210a-122">RELATED LINKS</span></span>

[<span data-ttu-id="d210a-123">New-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="d210a-123">New-AzureVNetGateway</span></span>](./New-AzureVNetGateway.md)

[<span data-ttu-id="d210a-124">Remove-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="d210a-124">Remove-AzureVNetGateway</span></span>](./Remove-AzureVNetGateway.md)

[<span data-ttu-id="d210a-125">Сброс — AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="d210a-125">Reset-AzureVNetGateway</span></span>](./Reset-AzureVNetGateway.md)

[<span data-ttu-id="d210a-126">Изменить размер — AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="d210a-126">Resize-AzureVNetGateway</span></span>](./Resize-AzureVNetGateway.md)

[<span data-ttu-id="d210a-127">Set-AzureVNetGatewayKey</span><span class="sxs-lookup"><span data-stu-id="d210a-127">Set-AzureVNetGatewayKey</span></span>](./Set-AzureVNetGatewayKey.md)


