---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 9FCECA04-9855-461C-9470-85312993C4B1
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5bb7bb3e708720b481edc4489d858c70736eac95
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076026"
---
# <span data-ttu-id="7ff0b-101">Start-AzureVNetGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="7ff0b-101">Start-AzureVNetGatewayDiagnostics</span></span>

## <span data-ttu-id="7ff0b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7ff0b-102">SYNOPSIS</span></span>
<span data-ttu-id="7ff0b-103">Запускает диагностику шлюза для VPN-шлюза.</span><span class="sxs-lookup"><span data-stu-id="7ff0b-103">Starts gateway diagnostics for a VPN gateway.</span></span>

## <span data-ttu-id="7ff0b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7ff0b-104">SYNTAX</span></span>

```
Start-AzureVNetGatewayDiagnostics -VNetName <String> -CaptureDurationInSeconds <Int32>
 [-ContainerName <String>] -StorageContext <AzureStorageContext> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="7ff0b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7ff0b-105">DESCRIPTION</span></span>
<span data-ttu-id="7ff0b-106">Командлет **Start-AzureVNetGatewayDiagnostics** запускает новый сеанс диагностики для шлюза виртуальной частной сети (VPN).</span><span class="sxs-lookup"><span data-stu-id="7ff0b-106">The **Start-AzureVNetGatewayDiagnostics** cmdlet starts a new gateway diagnostics session for a virtual private network (VPN) gateway.</span></span>
<span data-ttu-id="7ff0b-107">В каждый момент времени может выполняться только один сеанс диагностики шлюза.</span><span class="sxs-lookup"><span data-stu-id="7ff0b-107">Only one gateway diagnostics session can run at a time.</span></span>
<span data-ttu-id="7ff0b-108">Если вы запускаете этот командлет во время выполнения сеанса диагностики шлюза, этот командлет возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="7ff0b-108">If you run this cmdlet while a gateway diagnostics session is running, this cmdlet returns an error.</span></span>

## <span data-ttu-id="7ff0b-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7ff0b-109">EXAMPLES</span></span>

## <span data-ttu-id="7ff0b-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7ff0b-110">PARAMETERS</span></span>

### <span data-ttu-id="7ff0b-111">-CaptureDurationInSeconds</span><span class="sxs-lookup"><span data-stu-id="7ff0b-111">-CaptureDurationInSeconds</span></span>
<span data-ttu-id="7ff0b-112">Указывает продолжительность захвата в секундах.</span><span class="sxs-lookup"><span data-stu-id="7ff0b-112">Specifies the capture duration in seconds.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ff0b-113">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="7ff0b-113">-ContainerName</span></span>
<span data-ttu-id="7ff0b-114">Указывает имя контейнера Azure.</span><span class="sxs-lookup"><span data-stu-id="7ff0b-114">Specifies the name of an Azure container.</span></span>
<span data-ttu-id="7ff0b-115">Этот командлет хранит результаты в контейнере, указанном этим параметром.</span><span class="sxs-lookup"><span data-stu-id="7ff0b-115">This cmdlet stores results in the container that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ff0b-116">-Profile</span><span class="sxs-lookup"><span data-stu-id="7ff0b-116">-Profile</span></span>
<span data-ttu-id="7ff0b-117">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="7ff0b-117">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="7ff0b-118">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7ff0b-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7ff0b-119">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="7ff0b-119">-StorageContext</span></span>
<span data-ttu-id="7ff0b-120">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="7ff0b-120">Specifies an Azure storage context.</span></span>
<span data-ttu-id="7ff0b-121">Этот командлет хранит результаты с помощью контекста хранилища, который указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="7ff0b-121">This cmdlet stores results by using the storage context that this parameter specifies.</span></span>

```yaml
Type: AzureStorageContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ff0b-122">-VNetName</span><span class="sxs-lookup"><span data-stu-id="7ff0b-122">-VNetName</span></span>
<span data-ttu-id="7ff0b-123">Указывает виртуальную сеть, которая содержит шлюз виртуальной сети, для которого этот командлет выполняет диагностику.</span><span class="sxs-lookup"><span data-stu-id="7ff0b-123">Specifies the virtual network that contains a virtual network gateway for which this cmdlet runs diagnostics.</span></span>

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

### <span data-ttu-id="7ff0b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ff0b-124">CommonParameters</span></span>
<span data-ttu-id="7ff0b-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7ff0b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ff0b-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ff0b-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ff0b-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7ff0b-127">INPUTS</span></span>

## <span data-ttu-id="7ff0b-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7ff0b-128">OUTPUTS</span></span>

## <span data-ttu-id="7ff0b-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="7ff0b-129">NOTES</span></span>

## <span data-ttu-id="7ff0b-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7ff0b-130">RELATED LINKS</span></span>

[<span data-ttu-id="7ff0b-131">Get-AzureVNetGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="7ff0b-131">Get-AzureVNetGatewayDiagnostics</span></span>](./Get-AzureVNetGatewayDiagnostics.md)

[<span data-ttu-id="7ff0b-132">Остановить-AzureVNetGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="7ff0b-132">Stop-AzureVNetGatewayDiagnostics</span></span>](./Stop-AzureVNetGatewayDiagnostics.md)


