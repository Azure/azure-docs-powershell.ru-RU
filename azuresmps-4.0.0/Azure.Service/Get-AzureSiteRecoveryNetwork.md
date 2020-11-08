---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 615D2C5D-AB31-45DB-9535-9B9C8E957322
online version: ''
schema: 2.0.0
ms.openlocfilehash: 96b51b49d76093be96eeab26417f4a70f70c4627
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075592"
---
# <span data-ttu-id="065df-101">Get-AzureSiteRecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="065df-101">Get-AzureSiteRecoveryNetwork</span></span>

## <span data-ttu-id="065df-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="065df-102">SYNOPSIS</span></span>
<span data-ttu-id="065df-103">Возвращает сведения о сетях, управляемых восстановлением сайта для текущего хранилища.</span><span class="sxs-lookup"><span data-stu-id="065df-103">Gets information about the networks managed by Site Recovery for the current vault.</span></span>

## <span data-ttu-id="065df-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="065df-104">SYNTAX</span></span>

```
Get-AzureSiteRecoveryNetwork -Server <ASRServer> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="065df-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="065df-105">DESCRIPTION</span></span>
<span data-ttu-id="065df-106">Командлет **Get-AzureSiteRecoveryNetwork** получает сведения о сетях восстановления сайта Azure для текущего хранилища сайта.</span><span class="sxs-lookup"><span data-stu-id="065df-106">The **Get-AzureSiteRecoveryNetwork** cmdlet gets information about Azure Site Recovery networks for the current Site Recovery vault.</span></span>

## <span data-ttu-id="065df-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="065df-107">EXAMPLES</span></span>

### <span data-ttu-id="065df-108">Пример 1: получение сетей восстановления сайта</span><span class="sxs-lookup"><span data-stu-id="065df-108">Example 1: Get site recovery networks</span></span>
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> Get-AzureSiteRecoveryNetwork -Server $Servers[0]
Name                : phase2RecoveryVMNetwork
ID                  : 7cfd636e-5cc2-4e01-873b-8a7aa4962341
FabricObjectID      : 7cfd636e-5cc2-4e01-873b-8a7aa4962341
ServerId            : 774859b0-1966-48cc-9df7-759c441b7a8c
Type                : NoIsolation
FabricType          : VMM
VmNetworkSubnetList : {}

Name                : phase2PrimaryVMNetwork
ID                  : d903e2c6-3141-4cef-bfe1-04616cd43cbb
FabricObjectID      : d903e2c6-3141-4cef-bfe1-04616cd43cbb
ServerId            : 774859b0-1966-48cc-9df7-759c441b7a8c
Type                : NoIsolation
FabricType          : VMM
VmNetworkSubnetList : {}
```

<span data-ttu-id="065df-109">Первый командлет команды получает серверы для текущего хранилища Azure Site Recovery с помощью командлета **Get-AzureSiteRecoveryServer** .</span><span class="sxs-lookup"><span data-stu-id="065df-109">The first command cmdlet gets servers for the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryServer** cmdlet.</span></span>
<span data-ttu-id="065df-110">Команда хранит серверы восстановления сайта в переменной массива $Servers.</span><span class="sxs-lookup"><span data-stu-id="065df-110">The command stores the Site Recovery servers in the $Servers array variable.</span></span>

<span data-ttu-id="065df-111">Вторая команда возвращает сеть восстановления сайта для первого сервера в массиве $Servers.</span><span class="sxs-lookup"><span data-stu-id="065df-111">The second command gets the site recovery network for the first server in the $Servers array.</span></span>

## <span data-ttu-id="065df-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="065df-112">PARAMETERS</span></span>

### <span data-ttu-id="065df-113">-Profile</span><span class="sxs-lookup"><span data-stu-id="065df-113">-Profile</span></span>
<span data-ttu-id="065df-114">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="065df-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="065df-115">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="065df-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="065df-116">-Сервер</span><span class="sxs-lookup"><span data-stu-id="065df-116">-Server</span></span>
<span data-ttu-id="065df-117">Указывает сервер восстановления сайта.</span><span class="sxs-lookup"><span data-stu-id="065df-117">Specifies a Site Recovery server.</span></span>

```yaml
Type: ASRServer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="065df-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="065df-118">CommonParameters</span></span>
<span data-ttu-id="065df-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="065df-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="065df-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="065df-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="065df-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="065df-121">INPUTS</span></span>

## <span data-ttu-id="065df-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="065df-122">OUTPUTS</span></span>

## <span data-ttu-id="065df-123">Пуск</span><span class="sxs-lookup"><span data-stu-id="065df-123">NOTES</span></span>

## <span data-ttu-id="065df-124">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="065df-124">RELATED LINKS</span></span>

[<span data-ttu-id="065df-125">Командлеты служб Azure Site Recovery</span><span class="sxs-lookup"><span data-stu-id="065df-125">Azure Site Recovery Services Cmdlets</span></span>](./Azure.SiteRecoveryServices.md)


