---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/get-azblockchainmemberconsortiummember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainMemberConsortiumMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainMemberConsortiumMember.md
ms.openlocfilehash: f4dc342d72ce092a1f3cbd1695613fce2220661d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078485"
---
# <span data-ttu-id="2d8fa-101">Get-AzBlockchainMemberConsortiumMember</span><span class="sxs-lookup"><span data-stu-id="2d8fa-101">Get-AzBlockchainMemberConsortiumMember</span></span>

## <span data-ttu-id="2d8fa-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2d8fa-102">SYNOPSIS</span></span>
<span data-ttu-id="2d8fa-103">Список членов консорциума для blockchain участника.</span><span class="sxs-lookup"><span data-stu-id="2d8fa-103">Lists the consortium members for a blockchain member.</span></span>

## <span data-ttu-id="2d8fa-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2d8fa-104">SYNTAX</span></span>

```
Get-AzBlockchainMemberConsortiumMember -BlockchainMemberName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="2d8fa-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2d8fa-105">DESCRIPTION</span></span>
<span data-ttu-id="2d8fa-106">Список членов консорциума для blockchain участника.</span><span class="sxs-lookup"><span data-stu-id="2d8fa-106">Lists the consortium members for a blockchain member.</span></span>

## <span data-ttu-id="2d8fa-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2d8fa-107">EXAMPLES</span></span>

### <span data-ttu-id="2d8fa-108">Пример 1: список членов консорциума для blockchain участника.</span><span class="sxs-lookup"><span data-stu-id="2d8fa-108">Example 1: Lists the consortium members for a blockchain member.</span></span>
```powershell
PS C:\> Get-AzBlockchainMemberConsortiumMember -BlockchainMemberName dolauli001 -ResourceGroupName testgroup

DateModified          DisplayName JoinDate              Name       Role  Status SubscriptionId
------------          ----------- --------              ----       ----  ------ --------------
11/19/2019 5:14:41 AM dolauli001  11/19/2019 5:01:20 AM dolauli001 ADMIN Ready  c9cbd920-c00c-427c-852b-8aaf38badaeb
```

<span data-ttu-id="2d8fa-109">Эта команда перечисляет членов Consortium для blockchain участника.</span><span class="sxs-lookup"><span data-stu-id="2d8fa-109">This command lists the consortium members for a blockchain member.</span></span>

## <span data-ttu-id="2d8fa-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2d8fa-110">PARAMETERS</span></span>

### <span data-ttu-id="2d8fa-111">-BlockchainMemberName</span><span class="sxs-lookup"><span data-stu-id="2d8fa-111">-BlockchainMemberName</span></span>
<span data-ttu-id="2d8fa-112">Blockchain имя участника.</span><span class="sxs-lookup"><span data-stu-id="2d8fa-112">Blockchain member name.</span></span>

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

### <span data-ttu-id="2d8fa-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d8fa-113">-DefaultProfile</span></span>
<span data-ttu-id="2d8fa-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2d8fa-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2d8fa-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d8fa-115">-ResourceGroupName</span></span>
<span data-ttu-id="2d8fa-116">Имя группы ресурсов, содержащей ресурс.</span><span class="sxs-lookup"><span data-stu-id="2d8fa-116">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="2d8fa-117">Это значение можно получить в API-интерфейсе диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="2d8fa-117">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="2d8fa-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2d8fa-118">-SubscriptionId</span></span>
<span data-ttu-id="2d8fa-119">Получает идентификатор подписки, который однозначно определяет подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="2d8fa-119">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="2d8fa-120">Идентификатор подписки является частью универсального кода ресурса (URI) для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="2d8fa-120">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="2d8fa-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d8fa-121">CommonParameters</span></span>
<span data-ttu-id="2d8fa-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2d8fa-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d8fa-123">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2d8fa-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d8fa-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2d8fa-124">INPUTS</span></span>

## <span data-ttu-id="2d8fa-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2d8fa-125">OUTPUTS</span></span>

### <span data-ttu-id="2d8fa-126">Microsoft. Azure. PowerShell. командлеты. Blockchain. Models. Api20180601Preview. IConsortiumMember</span><span class="sxs-lookup"><span data-stu-id="2d8fa-126">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IConsortiumMember</span></span>

## <span data-ttu-id="2d8fa-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="2d8fa-127">NOTES</span></span>

<span data-ttu-id="2d8fa-128">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="2d8fa-128">ALIASES</span></span>

## <span data-ttu-id="2d8fa-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2d8fa-129">RELATED LINKS</span></span>

