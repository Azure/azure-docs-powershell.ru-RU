---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 706CBF65-C796-4525-BAEB-AAFAD44C0464
online version: ''
schema: 2.0.0
ms.openlocfilehash: d37c2ce3b32d23f7c5bb682d2116de84cc90f047
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076019"
---
# <span data-ttu-id="4b93f-101">Stop-AzureVNetGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="4b93f-101">Stop-AzureVNetGatewayDiagnostics</span></span>

## <span data-ttu-id="4b93f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4b93f-102">SYNOPSIS</span></span>
<span data-ttu-id="4b93f-103">Прекращение выполняющегося сеанса диагностики VPN-шлюза.</span><span class="sxs-lookup"><span data-stu-id="4b93f-103">Stops a running VPN gateway diagnostics session.</span></span>

## <span data-ttu-id="4b93f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4b93f-104">SYNTAX</span></span>

```
Stop-AzureVNetGatewayDiagnostics -VNetName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="4b93f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4b93f-105">DESCRIPTION</span></span>
<span data-ttu-id="4b93f-106">Командлет **Stop-AzureVNetGatewayDiagnostics** останавливает выполнение сеанса диагностики шлюза виртуальной частной сети (VPN).</span><span class="sxs-lookup"><span data-stu-id="4b93f-106">The **Stop-AzureVNetGatewayDiagnostics** cmdlet stops a running virtual private network (VPN) gateway diagnostics session.</span></span>
<span data-ttu-id="4b93f-107">Эта команда сохраняет результаты сеанса диагностики в учетной записи хранения, которую указывает командлет **Start-AzureVNetGatewayDiagnostics** .</span><span class="sxs-lookup"><span data-stu-id="4b93f-107">This command saves the results of the diagnostics session to the storage account that the **Start-AzureVNetGatewayDiagnostics** cmdlet specifies.</span></span>

## <span data-ttu-id="4b93f-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4b93f-108">EXAMPLES</span></span>

## <span data-ttu-id="4b93f-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4b93f-109">PARAMETERS</span></span>

### <span data-ttu-id="4b93f-110">-Profile</span><span class="sxs-lookup"><span data-stu-id="4b93f-110">-Profile</span></span>
<span data-ttu-id="4b93f-111">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="4b93f-111">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="4b93f-112">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="4b93f-112">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="4b93f-113">-VNetName</span><span class="sxs-lookup"><span data-stu-id="4b93f-113">-VNetName</span></span>
<span data-ttu-id="4b93f-114">Указывает виртуальную сеть, которая содержит шлюз виртуальной сети, для которого этот командлет останавливает диагностику.</span><span class="sxs-lookup"><span data-stu-id="4b93f-114">Specifies the virtual network that contains a virtual network gateway for which this cmdlet stops diagnostics.</span></span>

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

### <span data-ttu-id="4b93f-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b93f-115">CommonParameters</span></span>
<span data-ttu-id="4b93f-116">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4b93f-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b93f-117">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b93f-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b93f-118">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4b93f-118">INPUTS</span></span>

## <span data-ttu-id="4b93f-119">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4b93f-119">OUTPUTS</span></span>

## <span data-ttu-id="4b93f-120">Пуск</span><span class="sxs-lookup"><span data-stu-id="4b93f-120">NOTES</span></span>

## <span data-ttu-id="4b93f-121">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4b93f-121">RELATED LINKS</span></span>

[<span data-ttu-id="4b93f-122">Get-AzureVNetGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="4b93f-122">Get-AzureVNetGatewayDiagnostics</span></span>](./Get-AzureVNetGatewayDiagnostics.md)

[<span data-ttu-id="4b93f-123">Start-AzureVNetGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="4b93f-123">Start-AzureVNetGatewayDiagnostics</span></span>](./Start-AzureVNetGatewayDiagnostics.md)


