---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlreplica
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlReplica.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlReplica.md
ms.openlocfilehash: 80f9e645c1c906e8275d3e25fb2ab833befa9328
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243477"
---
# <span data-ttu-id="9a30c-101">Get-AzMySqlReplica</span><span class="sxs-lookup"><span data-stu-id="9a30c-101">Get-AzMySqlReplica</span></span>

## <span data-ttu-id="9a30c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9a30c-102">SYNOPSIS</span></span>
<span data-ttu-id="9a30c-103">Перечислите все реплики для данного сервера.</span><span class="sxs-lookup"><span data-stu-id="9a30c-103">List all the replicas for a given server.</span></span>

## <span data-ttu-id="9a30c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9a30c-104">SYNTAX</span></span>

```
Get-AzMySqlReplica -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="9a30c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9a30c-105">DESCRIPTION</span></span>
<span data-ttu-id="9a30c-106">Перечислите все реплики для данного сервера.</span><span class="sxs-lookup"><span data-stu-id="9a30c-106">List all the replicas for a given server.</span></span>

## <span data-ttu-id="9a30c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9a30c-107">EXAMPLES</span></span>

### <span data-ttu-id="9a30c-108">Пример 1: получение реплики сервера MySql по группе ресурсов и имени сервера</span><span class="sxs-lookup"><span data-stu-id="9a30c-108">Example 1: Get MySql server replica by resource group and server name</span></span>
```powershell
PS C:\> Get-AzMySqlReplica -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name               Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----               -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test-replica eastus   mysql_test         5.7     10240                   GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="9a30c-109">Этот командлет получает реплику сервера MySql по группе ресурсов и имени сервера.</span><span class="sxs-lookup"><span data-stu-id="9a30c-109">This cmdlet gets MySql server replica by resource group and server name.</span></span>

## <span data-ttu-id="9a30c-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9a30c-110">PARAMETERS</span></span>

### <span data-ttu-id="9a30c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a30c-111">-DefaultProfile</span></span>
<span data-ttu-id="9a30c-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9a30c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9a30c-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a30c-113">-ResourceGroupName</span></span>
<span data-ttu-id="9a30c-114">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9a30c-114">The name of the resource group.</span></span>
<span data-ttu-id="9a30c-115">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="9a30c-115">The name is case insensitive.</span></span>

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

### <span data-ttu-id="9a30c-116">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="9a30c-116">-ServerName</span></span>
<span data-ttu-id="9a30c-117">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="9a30c-117">The name of the server.</span></span>

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

### <span data-ttu-id="9a30c-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9a30c-118">-SubscriptionId</span></span>
<span data-ttu-id="9a30c-119">Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="9a30c-119">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="9a30c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a30c-120">CommonParameters</span></span>
<span data-ttu-id="9a30c-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9a30c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a30c-122">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9a30c-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a30c-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9a30c-123">INPUTS</span></span>

## <span data-ttu-id="9a30c-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9a30c-124">OUTPUTS</span></span>

### <span data-ttu-id="9a30c-125">Microsoft. Azure. PowerShell. командлеты. MySql. Models. Api20171201. IServer</span><span class="sxs-lookup"><span data-stu-id="9a30c-125">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="9a30c-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="9a30c-126">NOTES</span></span>

<span data-ttu-id="9a30c-127">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="9a30c-127">ALIASES</span></span>

## <span data-ttu-id="9a30c-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9a30c-128">RELATED LINKS</span></span>

