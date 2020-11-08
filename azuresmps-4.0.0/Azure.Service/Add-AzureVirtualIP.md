---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: FBED8515-4216-4AB6-B34E-D14A6063A3A7
online version: ''
schema: 2.0.0
ms.openlocfilehash: c2f145ec51bc6744d877661554e3d8e475d722fb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075713"
---
# <span data-ttu-id="e3c06-101">Add-AzureVirtualIP</span><span class="sxs-lookup"><span data-stu-id="e3c06-101">Add-AzureVirtualIP</span></span>

## <span data-ttu-id="e3c06-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e3c06-102">SYNOPSIS</span></span>
<span data-ttu-id="e3c06-103">Добавляет виртуальный IP-адрес в облачную службу.</span><span class="sxs-lookup"><span data-stu-id="e3c06-103">Adds a virtual IP to a cloud service.</span></span>

## <span data-ttu-id="e3c06-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e3c06-104">SYNTAX</span></span>

```
Add-AzureVirtualIP [-ServiceName] <String> [-VirtualIPName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="e3c06-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e3c06-105">DESCRIPTION</span></span>
<span data-ttu-id="e3c06-106">Командлет **Add-AzureVirtualIP** добавляет новый виртуальный IP-адрес (VIP) в службу Azure.</span><span class="sxs-lookup"><span data-stu-id="e3c06-106">The **Add-AzureVirtualIP** cmdlet adds a new virtual IP (VIP) to your Azure service.</span></span>
<span data-ttu-id="e3c06-107">У нового виртуального IP-адреса есть имя, но IP-адрес не выделен.</span><span class="sxs-lookup"><span data-stu-id="e3c06-107">The new virtual IP has a name but is not allocated an IP address.</span></span>

<span data-ttu-id="e3c06-108">IP-адрес выделяется только в том случае, если вы присоединяете конечную точку к VIP.</span><span class="sxs-lookup"><span data-stu-id="e3c06-108">The IP address is allocated only when you associate an endpoint to the VIP.</span></span>
<span data-ttu-id="e3c06-109">Дополнительные сведения вы видите в разделе Add-AzureEndpoint.</span><span class="sxs-lookup"><span data-stu-id="e3c06-109">See Add-AzureEndpoint for more details.</span></span>

<span data-ttu-id="e3c06-110">Подписка на план взимается для дополнительных IP VIP только после того, как они будут связаны с конечной точкой.</span><span class="sxs-lookup"><span data-stu-id="e3c06-110">Your subscription is charged for extra VIPs only once they are associated with an endpoint.</span></span>

## <span data-ttu-id="e3c06-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e3c06-111">EXAMPLES</span></span>

### <span data-ttu-id="e3c06-112">Пример 1: Добавление виртуального IP-адреса к службе</span><span class="sxs-lookup"><span data-stu-id="e3c06-112">Example 1: Add a virtual IP to a service</span></span>
```
PS C:\> Add-AzureVirtualIP -VirtualIPName "Vip01" -ServiceName "ContosoService03"
OperationDescription OperationId                          OperationStatus
-------------------- -----------                          ---------------
Add-AzureVirtualIP   4bd7b638-d2e7-216f-ba38-5221233d70ce Succeeded
```

<span data-ttu-id="e3c06-113">Эта команда добавляет виртуальный IP-адрес в службу.</span><span class="sxs-lookup"><span data-stu-id="e3c06-113">This command adds a virtual IP address to a service.</span></span>

## <span data-ttu-id="e3c06-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e3c06-114">PARAMETERS</span></span>

### <span data-ttu-id="e3c06-115">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="e3c06-115">-InformationAction</span></span>
<span data-ttu-id="e3c06-116">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="e3c06-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="e3c06-117">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="e3c06-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e3c06-118">Продолжал</span><span class="sxs-lookup"><span data-stu-id="e3c06-118">Continue</span></span>
- <span data-ttu-id="e3c06-119">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="e3c06-119">Ignore</span></span>
- <span data-ttu-id="e3c06-120">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="e3c06-120">Inquire</span></span>
- <span data-ttu-id="e3c06-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="e3c06-121">SilentlyContinue</span></span>
- <span data-ttu-id="e3c06-122">Остановить</span><span class="sxs-lookup"><span data-stu-id="e3c06-122">Stop</span></span>
- <span data-ttu-id="e3c06-123">Рвать</span><span class="sxs-lookup"><span data-stu-id="e3c06-123">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3c06-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="e3c06-124">-InformationVariable</span></span>
<span data-ttu-id="e3c06-125">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="e3c06-125">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3c06-126">-Profile</span><span class="sxs-lookup"><span data-stu-id="e3c06-126">-Profile</span></span>
<span data-ttu-id="e3c06-127">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="e3c06-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e3c06-128">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e3c06-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e3c06-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="e3c06-129">-ServiceName</span></span>
<span data-ttu-id="e3c06-130">Указывает имя службы.</span><span class="sxs-lookup"><span data-stu-id="e3c06-130">Specifies the name of the service.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3c06-131">-VirtualIPName</span><span class="sxs-lookup"><span data-stu-id="e3c06-131">-VirtualIPName</span></span>
<span data-ttu-id="e3c06-132">Указывает имя виртуального IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="e3c06-132">Specifies the name of the virtual IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3c06-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3c06-133">CommonParameters</span></span>
<span data-ttu-id="e3c06-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e3c06-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3c06-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3c06-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3c06-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e3c06-136">INPUTS</span></span>

## <span data-ttu-id="e3c06-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e3c06-137">OUTPUTS</span></span>

### <span data-ttu-id="e3c06-138">Microsoft. WindowsAzure. Commands. Utilities. Common. ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="e3c06-138">Microsoft.WindowsAzure.Commands.Utilities.Common.ManagementOperationContext</span></span>

## <span data-ttu-id="e3c06-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="e3c06-139">NOTES</span></span>

## <span data-ttu-id="e3c06-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e3c06-140">RELATED LINKS</span></span>

[<span data-ttu-id="e3c06-141">Add-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="e3c06-141">Add-AzureEndpoint</span></span>](./Add-AzureEndpoint.md)

[<span data-ttu-id="e3c06-142">Remove-AzureVirtualIP</span><span class="sxs-lookup"><span data-stu-id="e3c06-142">Remove-AzureVirtualIP</span></span>](./Remove-AzureVirtualIP.md)


