---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlflexibleserverreplica
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerReplica.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerReplica.md
ms.openlocfilehash: 77b1dae0db73a9a90a2100edef893edabfe87d0b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98518202"
---
# <span data-ttu-id="2acff-101">Get-AzMySqlFlexibleServerReplica</span><span class="sxs-lookup"><span data-stu-id="2acff-101">Get-AzMySqlFlexibleServerReplica</span></span>

## <span data-ttu-id="2acff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2acff-102">SYNOPSIS</span></span>
<span data-ttu-id="2acff-103">Укаймь все реплики для данного сервера.</span><span class="sxs-lookup"><span data-stu-id="2acff-103">List all the replicas for a given server.</span></span>

## <span data-ttu-id="2acff-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2acff-104">SYNTAX</span></span>

```
Get-AzMySqlFlexibleServerReplica -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="2acff-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2acff-105">DESCRIPTION</span></span>
<span data-ttu-id="2acff-106">Укаймь все реплики для данного сервера.</span><span class="sxs-lookup"><span data-stu-id="2acff-106">List all the replicas for a given server.</span></span>

## <span data-ttu-id="2acff-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2acff-107">EXAMPLES</span></span>

### <span data-ttu-id="2acff-108">Пример 1. Получить репликацию сервера MySql по имени группы ресурсов и сервера</span><span class="sxs-lookup"><span data-stu-id="2acff-108">Example 1: Get MySql server replica by resource group and server name</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServerReplica -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- ---------------- -------------
mysql-test    westus2   mysql_test         5.7     5120                    Standard_D2ds_v4 GeneralPurpose
```

<span data-ttu-id="2acff-109">Этот cmdlet получает репликацию сервера MySql по группе ресурсов и имени сервера.</span><span class="sxs-lookup"><span data-stu-id="2acff-109">This cmdlet gets MySql server replica by resource group and server name.</span></span>

## <span data-ttu-id="2acff-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2acff-110">PARAMETERS</span></span>

### <span data-ttu-id="2acff-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2acff-111">-DefaultProfile</span></span>
<span data-ttu-id="2acff-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2acff-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2acff-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2acff-113">-ResourceGroupName</span></span>
<span data-ttu-id="2acff-114">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2acff-114">The name of the resource group.</span></span>
<span data-ttu-id="2acff-115">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="2acff-115">The name is case insensitive.</span></span>

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

### <span data-ttu-id="2acff-116">-ServerName</span><span class="sxs-lookup"><span data-stu-id="2acff-116">-ServerName</span></span>
<span data-ttu-id="2acff-117">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="2acff-117">The name of the server.</span></span>

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

### <span data-ttu-id="2acff-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2acff-118">-SubscriptionId</span></span>
<span data-ttu-id="2acff-119">ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="2acff-119">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="2acff-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2acff-120">CommonParameters</span></span>
<span data-ttu-id="2acff-121">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2acff-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2acff-122">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2acff-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2acff-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2acff-123">INPUTS</span></span>

## <span data-ttu-id="2acff-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2acff-124">OUTPUTS</span></span>

### <span data-ttu-id="2acff-125">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IServerAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="2acff-125">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IServerAutoGenerated</span></span>

## <span data-ttu-id="2acff-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2acff-126">NOTES</span></span>

<span data-ttu-id="2acff-127">ALIASES</span><span class="sxs-lookup"><span data-stu-id="2acff-127">ALIASES</span></span>

## <span data-ttu-id="2acff-128">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2acff-128">RELATED LINKS</span></span>

