---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/get-azmariadbreplica
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbReplica.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbReplica.md
ms.openlocfilehash: 336360c3c7aac901ae90ea02f4832a066c6fff12
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248905"
---
# <span data-ttu-id="47509-101">Get-AzMariaDbReplica</span><span class="sxs-lookup"><span data-stu-id="47509-101">Get-AzMariaDbReplica</span></span>

## <span data-ttu-id="47509-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="47509-102">SYNOPSIS</span></span>
<span data-ttu-id="47509-103">Перечислите все реплики для данного сервера.</span><span class="sxs-lookup"><span data-stu-id="47509-103">List all the replicas for a given server.</span></span>

## <span data-ttu-id="47509-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="47509-104">SYNTAX</span></span>

```
Get-AzMariaDbReplica -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="47509-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="47509-105">DESCRIPTION</span></span>
<span data-ttu-id="47509-106">Перечислите все реплики для данного сервера.</span><span class="sxs-lookup"><span data-stu-id="47509-106">List all the replicas for a given server.</span></span>

## <span data-ttu-id="47509-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="47509-107">EXAMPLES</span></span>

### <span data-ttu-id="47509-108">Пример 1: список всех баз данных реплики в MariaDB</span><span class="sxs-lookup"><span data-stu-id="47509-108">Example 1: List all replica DB under a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbReplica -ServerName mariadb-test-szp6dt -ResourceGroupName mariadb-test-qu5ov0

Name                       Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                       -------- ------------------ ------- ----------------------- -------   -------        --------------
mariadb-test-szp6dt-rep428 eastus   zmoxhpgjqc         10.2    5120                    GP_Gen5_4 GeneralPurpose Enabled
mariadb-test-szp6dt-rep154 eastus   zcsxhpasdc         10.2    5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="47509-109">Эта команда выводит все базы данных реплики в MariaDB.</span><span class="sxs-lookup"><span data-stu-id="47509-109">This command lists all replica DB under a MariaDB.</span></span>

## <span data-ttu-id="47509-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="47509-110">PARAMETERS</span></span>

### <span data-ttu-id="47509-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47509-111">-DefaultProfile</span></span>
<span data-ttu-id="47509-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="47509-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47509-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47509-113">-ResourceGroupName</span></span>
<span data-ttu-id="47509-114">Имя группы ресурсов, содержащей ресурс.</span><span class="sxs-lookup"><span data-stu-id="47509-114">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="47509-115">Это значение можно получить в API-интерфейсе диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="47509-115">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="47509-116">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="47509-116">-ServerName</span></span>
<span data-ttu-id="47509-117">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="47509-117">The name of the server.</span></span>

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

### <span data-ttu-id="47509-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="47509-118">-SubscriptionId</span></span>
<span data-ttu-id="47509-119">Идентификатор подписки, определяющий подписку на Azure.</span><span class="sxs-lookup"><span data-stu-id="47509-119">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="47509-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47509-120">CommonParameters</span></span>
<span data-ttu-id="47509-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="47509-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47509-122">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="47509-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47509-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="47509-123">INPUTS</span></span>

## <span data-ttu-id="47509-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="47509-124">OUTPUTS</span></span>

### <span data-ttu-id="47509-125">Microsoft. Azure. PowerShell. командлеты. MariaDb. Models. Api20180601Preview. IServer</span><span class="sxs-lookup"><span data-stu-id="47509-125">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="47509-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="47509-126">NOTES</span></span>

<span data-ttu-id="47509-127">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="47509-127">ALIASES</span></span>

## <span data-ttu-id="47509-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="47509-128">RELATED LINKS</span></span>

