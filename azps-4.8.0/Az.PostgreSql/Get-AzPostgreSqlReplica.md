---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/get-azpostgresqlreplica
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlReplica.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlReplica.md
ms.openlocfilehash: 5d27610924fe0b4a92acfb5f7d1e678742d5b5c7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244268"
---
# <span data-ttu-id="0c6a5-101">Get-AzPostgreSqlReplica</span><span class="sxs-lookup"><span data-stu-id="0c6a5-101">Get-AzPostgreSqlReplica</span></span>

## <span data-ttu-id="0c6a5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0c6a5-102">SYNOPSIS</span></span>
<span data-ttu-id="0c6a5-103">Перечислите все реплики для данного сервера.</span><span class="sxs-lookup"><span data-stu-id="0c6a5-103">List all the replicas for a given server.</span></span>

## <span data-ttu-id="0c6a5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0c6a5-104">SYNTAX</span></span>

```
Get-AzPostgreSqlReplica -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="0c6a5-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0c6a5-105">DESCRIPTION</span></span>
<span data-ttu-id="0c6a5-106">Перечислите все реплики для данного сервера.</span><span class="sxs-lookup"><span data-stu-id="0c6a5-106">List all the replicas for a given server.</span></span>

## <span data-ttu-id="0c6a5-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0c6a5-107">EXAMPLES</span></span>

### <span data-ttu-id="0c6a5-108">Пример 1: получение реплики сервера PostgreSql по группе ресурсов и имени сервера</span><span class="sxs-lookup"><span data-stu-id="0c6a5-108">Example 1: Get PostgreSql server replica by resource group and server name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlReplica -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer

Name                        Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                        -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserverreplica eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="0c6a5-109">Этот командлет получает PostgreSql реплики сервера по группе ресурсов и имени сервера.</span><span class="sxs-lookup"><span data-stu-id="0c6a5-109">This cmdlet gets PostgreSql server replica by resource group and server name.</span></span>

## <span data-ttu-id="0c6a5-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0c6a5-110">PARAMETERS</span></span>

### <span data-ttu-id="0c6a5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c6a5-111">-DefaultProfile</span></span>
<span data-ttu-id="0c6a5-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0c6a5-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0c6a5-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c6a5-113">-ResourceGroupName</span></span>
<span data-ttu-id="0c6a5-114">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0c6a5-114">The name of the resource group.</span></span>
<span data-ttu-id="0c6a5-115">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="0c6a5-115">The name is case insensitive.</span></span>

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

### <span data-ttu-id="0c6a5-116">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="0c6a5-116">-ServerName</span></span>
<span data-ttu-id="0c6a5-117">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="0c6a5-117">The name of the server.</span></span>

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

### <span data-ttu-id="0c6a5-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0c6a5-118">-SubscriptionId</span></span>
<span data-ttu-id="0c6a5-119">Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="0c6a5-119">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="0c6a5-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c6a5-120">CommonParameters</span></span>
<span data-ttu-id="0c6a5-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0c6a5-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c6a5-122">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0c6a5-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c6a5-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0c6a5-123">INPUTS</span></span>

## <span data-ttu-id="0c6a5-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0c6a5-124">OUTPUTS</span></span>

### <span data-ttu-id="0c6a5-125">Microsoft. Azure. PowerShell. командлеты. PostgreSql. Models. Api20171201. IServer</span><span class="sxs-lookup"><span data-stu-id="0c6a5-125">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="0c6a5-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="0c6a5-126">NOTES</span></span>

<span data-ttu-id="0c6a5-127">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="0c6a5-127">ALIASES</span></span>

## <span data-ttu-id="0c6a5-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0c6a5-128">RELATED LINKS</span></span>

