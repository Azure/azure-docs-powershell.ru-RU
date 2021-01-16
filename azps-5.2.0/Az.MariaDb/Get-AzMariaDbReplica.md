---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/get-azmariadbreplica
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbReplica.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbReplica.md
ms.openlocfilehash: 336360c3c7aac901ae90ea02f4832a066c6fff12
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98324145"
---
# <span data-ttu-id="5b9e6-101">Get-AzMariaDbReplica</span><span class="sxs-lookup"><span data-stu-id="5b9e6-101">Get-AzMariaDbReplica</span></span>

## <span data-ttu-id="5b9e6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5b9e6-102">SYNOPSIS</span></span>
<span data-ttu-id="5b9e6-103">Перечислить все реплики для данного сервера.</span><span class="sxs-lookup"><span data-stu-id="5b9e6-103">List all the replicas for a given server.</span></span>

## <span data-ttu-id="5b9e6-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5b9e6-104">SYNTAX</span></span>

```
Get-AzMariaDbReplica -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="5b9e6-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5b9e6-105">DESCRIPTION</span></span>
<span data-ttu-id="5b9e6-106">Перечислить все реплики для данного сервера.</span><span class="sxs-lookup"><span data-stu-id="5b9e6-106">List all the replicas for a given server.</span></span>

## <span data-ttu-id="5b9e6-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5b9e6-107">EXAMPLES</span></span>

### <span data-ttu-id="5b9e6-108">Пример 1. List all replica DB under a MariaDB</span><span class="sxs-lookup"><span data-stu-id="5b9e6-108">Example 1: List all replica DB under a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbReplica -ServerName mariadb-test-szp6dt -ResourceGroupName mariadb-test-qu5ov0

Name                       Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                       -------- ------------------ ------- ----------------------- -------   -------        --------------
mariadb-test-szp6dt-rep428 eastus   zmoxhpgjqc         10.2    5120                    GP_Gen5_4 GeneralPurpose Enabled
mariadb-test-szp6dt-rep154 eastus   zcsxhpasdc         10.2    5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="5b9e6-109">В этой команде перечислены все реплицируемые DB в соответствии с MariaDB.</span><span class="sxs-lookup"><span data-stu-id="5b9e6-109">This command lists all replica DB under a MariaDB.</span></span>

## <span data-ttu-id="5b9e6-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5b9e6-110">PARAMETERS</span></span>

### <span data-ttu-id="5b9e6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b9e6-111">-DefaultProfile</span></span>
<span data-ttu-id="5b9e6-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5b9e6-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b9e6-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b9e6-113">-ResourceGroupName</span></span>
<span data-ttu-id="5b9e6-114">Имя группы ресурсов, которая содержит ресурс.</span><span class="sxs-lookup"><span data-stu-id="5b9e6-114">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="5b9e6-115">Это значение можно получить через API Диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="5b9e6-115">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="5b9e6-116">-ServerName</span><span class="sxs-lookup"><span data-stu-id="5b9e6-116">-ServerName</span></span>
<span data-ttu-id="5b9e6-117">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="5b9e6-117">The name of the server.</span></span>

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

### <span data-ttu-id="5b9e6-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5b9e6-118">-SubscriptionId</span></span>
<span data-ttu-id="5b9e6-119">Идентификатор подписки, который определяет подписку Azure.</span><span class="sxs-lookup"><span data-stu-id="5b9e6-119">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="5b9e6-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b9e6-120">CommonParameters</span></span>
<span data-ttu-id="5b9e6-121">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b9e6-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b9e6-122">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5b9e6-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b9e6-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5b9e6-123">INPUTS</span></span>

## <span data-ttu-id="5b9e6-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5b9e6-124">OUTPUTS</span></span>

### <span data-ttu-id="5b9e6-125">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span><span class="sxs-lookup"><span data-stu-id="5b9e6-125">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="5b9e6-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5b9e6-126">NOTES</span></span>

<span data-ttu-id="5b9e6-127">ALIASES</span><span class="sxs-lookup"><span data-stu-id="5b9e6-127">ALIASES</span></span>

## <span data-ttu-id="5b9e6-128">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5b9e6-128">RELATED LINKS</span></span>

