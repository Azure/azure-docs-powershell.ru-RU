---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 615D2C5D-AB31-45DB-9535-9B9C8E957322
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4a5701fc6308f1884bbf0237887a223a62a58669
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100411591"
---
# <span data-ttu-id="5e00a-101">Get-AzureSiteRecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="5e00a-101">Get-AzureSiteRecoveryNetwork</span></span>

## <span data-ttu-id="5e00a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5e00a-102">SYNOPSIS</span></span>
<span data-ttu-id="5e00a-103">Получает сведения о сетях, управляемых восстановлением сайта для текущего хранилища.</span><span class="sxs-lookup"><span data-stu-id="5e00a-103">Gets information about the networks managed by Site Recovery for the current vault.</span></span>

## <span data-ttu-id="5e00a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5e00a-104">SYNTAX</span></span>

```
Get-AzureSiteRecoveryNetwork -Server <ASRServer> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="5e00a-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5e00a-105">DESCRIPTION</span></span>
<span data-ttu-id="5e00a-106">Командлет **Get-AzureSiteRecoveryNetwork** получает сведения о сетях восстановления сайтов Azure для текущего хранилища восстановления сайта.</span><span class="sxs-lookup"><span data-stu-id="5e00a-106">The **Get-AzureSiteRecoveryNetwork** cmdlet gets information about Azure Site Recovery networks for the current Site Recovery vault.</span></span>

## <span data-ttu-id="5e00a-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5e00a-107">EXAMPLES</span></span>

### <span data-ttu-id="5e00a-108">Пример 1. Получить сети восстановления сайта</span><span class="sxs-lookup"><span data-stu-id="5e00a-108">Example 1: Get site recovery networks</span></span>
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

<span data-ttu-id="5e00a-109">Первая команда получает серверы для текущего хранилища восстановления сайта Azure с помощью командлета **Get-AzureSiteRecoveryServer.**</span><span class="sxs-lookup"><span data-stu-id="5e00a-109">The first command cmdlet gets servers for the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryServer** cmdlet.</span></span>
<span data-ttu-id="5e00a-110">Команда сохраняет серверы восстановления сайта в переменной $Servers массива.</span><span class="sxs-lookup"><span data-stu-id="5e00a-110">The command stores the Site Recovery servers in the $Servers array variable.</span></span>

<span data-ttu-id="5e00a-111">Вторая команда получает сеть восстановления сайта для первого сервера в $Servers массиве.</span><span class="sxs-lookup"><span data-stu-id="5e00a-111">The second command gets the site recovery network for the first server in the $Servers array.</span></span>

## <span data-ttu-id="5e00a-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5e00a-112">PARAMETERS</span></span>

### <span data-ttu-id="5e00a-113">-Profile</span><span class="sxs-lookup"><span data-stu-id="5e00a-113">-Profile</span></span>
<span data-ttu-id="5e00a-114">Определяет профиль Azure, для которого читается этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5e00a-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5e00a-115">Если не указать профиль, этот cmdlet будет читать данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5e00a-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="5e00a-116">-Server</span><span class="sxs-lookup"><span data-stu-id="5e00a-116">-Server</span></span>
<span data-ttu-id="5e00a-117">Указывает сервер восстановления сайта.</span><span class="sxs-lookup"><span data-stu-id="5e00a-117">Specifies a Site Recovery server.</span></span>

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

### <span data-ttu-id="5e00a-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e00a-118">CommonParameters</span></span>
<span data-ttu-id="5e00a-119">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e00a-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e00a-120">Дополнительные сведения см. в about_CommonParameters https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e00a-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e00a-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5e00a-121">INPUTS</span></span>

## <span data-ttu-id="5e00a-122">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5e00a-122">OUTPUTS</span></span>

## <span data-ttu-id="5e00a-123">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5e00a-123">NOTES</span></span>

## <span data-ttu-id="5e00a-124">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5e00a-124">RELATED LINKS</span></span>




