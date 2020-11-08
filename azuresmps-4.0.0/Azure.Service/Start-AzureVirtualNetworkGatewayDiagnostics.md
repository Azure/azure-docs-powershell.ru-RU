---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: DA5689DF-AA4A-4161-89B0-8055BF384274
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7b71367ac18a753fad5425d0073b55cacb413e4b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075772"
---
# <span data-ttu-id="ccf6f-101">Start-AzureVirtualNetworkGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="ccf6f-101">Start-AzureVirtualNetworkGatewayDiagnostics</span></span>

## <span data-ttu-id="ccf6f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ccf6f-102">SYNOPSIS</span></span>
<span data-ttu-id="ccf6f-103">Запускает диагностику для шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="ccf6f-103">Starts diagnostics for a virtual network gateway.</span></span>

## <span data-ttu-id="ccf6f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ccf6f-104">SYNTAX</span></span>

```
Start-AzureVirtualNetworkGatewayDiagnostics -GatewayId <String> [-CaptureDurationInSeconds <Int32>]
 [-ContainerName <String>] [-StorageContext <AzureStorageContext>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="ccf6f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ccf6f-105">DESCRIPTION</span></span>
<span data-ttu-id="ccf6f-106">Командлет **Start-AzureVirtualNetworkGatewayDiagnostics** запускает новый сеанс диагностики для шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="ccf6f-106">The **Start-AzureVirtualNetworkGatewayDiagnostics** cmdlet starts a new gateway diagnostics session for a virtual network gateway.</span></span>
<span data-ttu-id="ccf6f-107">В каждый момент времени может выполняться только один сеанс диагностики шлюза.</span><span class="sxs-lookup"><span data-stu-id="ccf6f-107">Only one gateway diagnostics session can run at a time.</span></span>
<span data-ttu-id="ccf6f-108">Если вы запускаете этот командлет во время выполнения сеанса диагностики шлюза, этот командлет возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="ccf6f-108">If you run this cmdlet while a gateway diagnostics session is running, this cmdlet returns an error.</span></span>

## <span data-ttu-id="ccf6f-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ccf6f-109">EXAMPLES</span></span>

## <span data-ttu-id="ccf6f-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ccf6f-110">PARAMETERS</span></span>

### <span data-ttu-id="ccf6f-111">-CaptureDurationInSeconds</span><span class="sxs-lookup"><span data-stu-id="ccf6f-111">-CaptureDurationInSeconds</span></span>
<span data-ttu-id="ccf6f-112">Указывает продолжительность захвата в секундах.</span><span class="sxs-lookup"><span data-stu-id="ccf6f-112">Specifies the capture duration in seconds.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccf6f-113">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="ccf6f-113">-ContainerName</span></span>
<span data-ttu-id="ccf6f-114">Указывает имя контейнера Azure.</span><span class="sxs-lookup"><span data-stu-id="ccf6f-114">Specifies the name of an Azure container.</span></span>
<span data-ttu-id="ccf6f-115">Этот командлет хранит результаты в контейнере, указанном этим параметром.</span><span class="sxs-lookup"><span data-stu-id="ccf6f-115">This cmdlet stores results in the container that this parameter specifies.</span></span>

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

### <span data-ttu-id="ccf6f-116">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="ccf6f-116">-GatewayId</span></span>
<span data-ttu-id="ccf6f-117">Указывает идентификатор шлюза.</span><span class="sxs-lookup"><span data-stu-id="ccf6f-117">Specifies the ID of a gateway.</span></span>

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

### <span data-ttu-id="ccf6f-118">-Profile</span><span class="sxs-lookup"><span data-stu-id="ccf6f-118">-Profile</span></span>
<span data-ttu-id="ccf6f-119">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="ccf6f-119">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="ccf6f-120">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ccf6f-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ccf6f-121">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="ccf6f-121">-StorageContext</span></span>
<span data-ttu-id="ccf6f-122">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="ccf6f-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="ccf6f-123">Этот командлет хранит результаты с помощью контекста хранилища, который указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="ccf6f-123">This cmdlet stores results by using the storage context that this parameter specifies.</span></span>

```yaml
Type: AzureStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccf6f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccf6f-124">CommonParameters</span></span>
<span data-ttu-id="ccf6f-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ccf6f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccf6f-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ccf6f-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccf6f-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ccf6f-127">INPUTS</span></span>

## <span data-ttu-id="ccf6f-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ccf6f-128">OUTPUTS</span></span>

## <span data-ttu-id="ccf6f-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="ccf6f-129">NOTES</span></span>

## <span data-ttu-id="ccf6f-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ccf6f-130">RELATED LINKS</span></span>

[<span data-ttu-id="ccf6f-131">Get-AzureVirtualNetworkGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="ccf6f-131">Get-AzureVirtualNetworkGatewayDiagnostics</span></span>](./Get-AzureVirtualNetworkGatewayDiagnostics.md)

[<span data-ttu-id="ccf6f-132">Остановить-AzureVirtualNetworkGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="ccf6f-132">Stop-AzureVirtualNetworkGatewayDiagnostics</span></span>](./Stop-AzureVirtualNetworkGatewayDiagnostics.md)


