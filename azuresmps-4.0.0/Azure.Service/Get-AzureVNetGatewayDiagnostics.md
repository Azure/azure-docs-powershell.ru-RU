---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 22E8CB18-8CDD-4992-AB81-E1BB400E6BC7
online version: ''
schema: 2.0.0
ms.openlocfilehash: 294e931529b7de939a6a5c20181d48b18da1e892
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076277"
---
# <span data-ttu-id="f1e9d-101">Get-AzureVNetGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="f1e9d-101">Get-AzureVNetGatewayDiagnostics</span></span>

## <span data-ttu-id="f1e9d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f1e9d-102">SYNOPSIS</span></span>
<span data-ttu-id="f1e9d-103">Получает текущее состояние диагностики для шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="f1e9d-103">Gets the current state of diagnostics for a virtual network gateway.</span></span>

## <span data-ttu-id="f1e9d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f1e9d-104">SYNTAX</span></span>

```
Get-AzureVNetGatewayDiagnostics -VNetName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="f1e9d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f1e9d-105">DESCRIPTION</span></span>
<span data-ttu-id="f1e9d-106">Командлет **Get-AzureVNetGatewayDiagnostics** получает текущее состояние диагностики для шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="f1e9d-106">The **Get-AzureVNetGatewayDiagnostics** cmdlet gets the current state of diagnostics for a virtual network gateway.</span></span>
<span data-ttu-id="f1e9d-107">Если существует большой двоичный объект (BLOB), где **Start-AzureVNetGatewayDiagnostics** сохраняет предыдущий сеанс диагностики, этот командлет также возвращает URL-адрес большого двоичного объекта, в котором командлет сохранил этот сеанс диагностики.</span><span class="sxs-lookup"><span data-stu-id="f1e9d-107">If a binary large object (blob) exists where the **Start-AzureVNetGatewayDiagnostics** saved a previous diagnostics session, this cmdlet also returns the URL of the blob where that cmdlet saved that diagnostics session.</span></span>

## <span data-ttu-id="f1e9d-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f1e9d-108">EXAMPLES</span></span>

## <span data-ttu-id="f1e9d-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f1e9d-109">PARAMETERS</span></span>

### <span data-ttu-id="f1e9d-110">-Profile</span><span class="sxs-lookup"><span data-stu-id="f1e9d-110">-Profile</span></span>
<span data-ttu-id="f1e9d-111">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="f1e9d-111">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="f1e9d-112">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f1e9d-112">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f1e9d-113">-VNetName</span><span class="sxs-lookup"><span data-stu-id="f1e9d-113">-VNetName</span></span>
<span data-ttu-id="f1e9d-114">Указывает виртуальную сеть, которая содержит шлюз виртуальной сети, для которого этот командлет получает диагностику.</span><span class="sxs-lookup"><span data-stu-id="f1e9d-114">Specifies the virtual network that contains a virtual network gateway for which this cmdlet gets diagnostics.</span></span>

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

### <span data-ttu-id="f1e9d-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1e9d-115">CommonParameters</span></span>
<span data-ttu-id="f1e9d-116">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f1e9d-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1e9d-117">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1e9d-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1e9d-118">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f1e9d-118">INPUTS</span></span>

## <span data-ttu-id="f1e9d-119">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f1e9d-119">OUTPUTS</span></span>

## <span data-ttu-id="f1e9d-120">Пуск</span><span class="sxs-lookup"><span data-stu-id="f1e9d-120">NOTES</span></span>

## <span data-ttu-id="f1e9d-121">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f1e9d-121">RELATED LINKS</span></span>

[<span data-ttu-id="f1e9d-122">Start-AzureVNetGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="f1e9d-122">Start-AzureVNetGatewayDiagnostics</span></span>](./Start-AzureVNetGatewayDiagnostics.md)

[<span data-ttu-id="f1e9d-123">Остановить-AzureVNetGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="f1e9d-123">Stop-AzureVNetGatewayDiagnostics</span></span>](./Stop-AzureVNetGatewayDiagnostics.md)


