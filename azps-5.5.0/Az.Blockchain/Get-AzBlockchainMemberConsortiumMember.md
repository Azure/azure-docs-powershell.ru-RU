---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/get-azblockchainmemberconsortiummember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainMemberConsortiumMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainMemberConsortiumMember.md
ms.openlocfilehash: f4dc342d72ce092a1f3cbd1695613fce2220661d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100234996"
---
# <span data-ttu-id="c8b14-101">Get-AzBlockchainMemberConsortiumMember</span><span class="sxs-lookup"><span data-stu-id="c8b14-101">Get-AzBlockchainMemberConsortiumMember</span></span>

## <span data-ttu-id="c8b14-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c8b14-102">SYNOPSIS</span></span>
<span data-ttu-id="c8b14-103">Список участников от консорциума в качестве участника- участника.</span><span class="sxs-lookup"><span data-stu-id="c8b14-103">Lists the consortium members for a blockchain member.</span></span>

## <span data-ttu-id="c8b14-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c8b14-104">SYNTAX</span></span>

```
Get-AzBlockchainMemberConsortiumMember -BlockchainMemberName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="c8b14-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c8b14-105">DESCRIPTION</span></span>
<span data-ttu-id="c8b14-106">Список участников от консорциума в качестве участника- участника.</span><span class="sxs-lookup"><span data-stu-id="c8b14-106">Lists the consortium members for a blockchain member.</span></span>

## <span data-ttu-id="c8b14-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c8b14-107">EXAMPLES</span></span>

### <span data-ttu-id="c8b14-108">Пример 1. Список участников от консорциума в качестве участника- участника.</span><span class="sxs-lookup"><span data-stu-id="c8b14-108">Example 1: Lists the consortium members for a blockchain member.</span></span>
```powershell
PS C:\> Get-AzBlockchainMemberConsortiumMember -BlockchainMemberName dolauli001 -ResourceGroupName testgroup

DateModified          DisplayName JoinDate              Name       Role  Status SubscriptionId
------------          ----------- --------              ----       ----  ------ --------------
11/19/2019 5:14:41 AM dolauli001  11/19/2019 5:01:20 AM dolauli001 ADMIN Ready  c9cbd920-c00c-427c-852b-8aaf38badaeb
```

<span data-ttu-id="c8b14-109">Эта команда содержит список участников от консорциума в качестве участника.</span><span class="sxs-lookup"><span data-stu-id="c8b14-109">This command lists the consortium members for a blockchain member.</span></span>

## <span data-ttu-id="c8b14-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c8b14-110">PARAMETERS</span></span>

### <span data-ttu-id="c8b14-111">-ДолжныеИмяЯ</span><span class="sxs-lookup"><span data-stu-id="c8b14-111">-BlockchainMemberName</span></span>
<span data-ttu-id="c8b14-112">Имя участника.</span><span class="sxs-lookup"><span data-stu-id="c8b14-112">Blockchain member name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8b14-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8b14-113">-DefaultProfile</span></span>
<span data-ttu-id="c8b14-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c8b14-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8b14-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8b14-115">-ResourceGroupName</span></span>
<span data-ttu-id="c8b14-116">Имя группы ресурсов, которая содержит ресурс.</span><span class="sxs-lookup"><span data-stu-id="c8b14-116">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="c8b14-117">Это значение можно получить через API Диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="c8b14-117">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8b14-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c8b14-118">-SubscriptionId</span></span>
<span data-ttu-id="c8b14-119">Возвращает идентификатор подписки, который однозначно определяет подписку на Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="c8b14-119">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="c8b14-120">Этот ИД подписки является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="c8b14-120">The subscription ID is part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8b14-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8b14-121">CommonParameters</span></span>
<span data-ttu-id="c8b14-122">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8b14-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8b14-123">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c8b14-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8b14-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c8b14-124">INPUTS</span></span>

## <span data-ttu-id="c8b14-125">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c8b14-125">OUTPUTS</span></span>

### <span data-ttu-id="c8b14-126">Microsoft.Azure.PowerShell.Cmdlets.Models.Api20180601Preview.IConsortiumMember</span><span class="sxs-lookup"><span data-stu-id="c8b14-126">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IConsortiumMember</span></span>

## <span data-ttu-id="c8b14-127">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c8b14-127">NOTES</span></span>

<span data-ttu-id="c8b14-128">ALIASES</span><span class="sxs-lookup"><span data-stu-id="c8b14-128">ALIASES</span></span>

## <span data-ttu-id="c8b14-129">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c8b14-129">RELATED LINKS</span></span>

