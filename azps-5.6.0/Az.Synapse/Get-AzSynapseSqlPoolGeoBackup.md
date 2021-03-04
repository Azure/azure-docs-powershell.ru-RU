---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsesqlpoolgeobackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolGeoBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolGeoBackup.md
ms.openlocfilehash: d1c0b6439b148d51506861a6bfffc6a6681343ef
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101957864"
---
# <span data-ttu-id="9b2d9-101">Get-AzSynapseSqlPoolGeoBackup</span><span class="sxs-lookup"><span data-stu-id="9b2d9-101">Get-AzSynapseSqlPoolGeoBackup</span></span>

## <span data-ttu-id="9b2d9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9b2d9-102">SYNOPSIS</span></span>
<span data-ttu-id="9b2d9-103">Получает гео избыточное резервное копирование пула Sql.</span><span class="sxs-lookup"><span data-stu-id="9b2d9-103">Gets a geo-redundant backup of a Sql Pool.</span></span>

## <span data-ttu-id="9b2d9-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9b2d9-104">SYNTAX</span></span>

### <span data-ttu-id="9b2d9-105">GetByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9b2d9-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlPoolGeoBackup [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9b2d9-106">SqlPoolGeoBackupResourceId</span><span class="sxs-lookup"><span data-stu-id="9b2d9-106">SqlPoolGeoBackupResourceId</span></span>
```
Get-AzSynapseSqlPoolGeoBackup [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9b2d9-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9b2d9-107">DESCRIPTION</span></span>
<span data-ttu-id="9b2d9-108">Cmdlet **Get-AzSynapseSqlPoolGeoBackup** получает указанное геоизбыточное резервное копирование пула SQL или все доступные геоизбытные резервные копии в указанной рабочей области.</span><span class="sxs-lookup"><span data-stu-id="9b2d9-108">The **Get-AzSynapseSqlPoolGeoBackup** cmdlet gets a specified geo-redundant backup of a SQL Pool or all available geo-redundant backups on a specified workspace.</span></span>
<span data-ttu-id="9b2d9-109">Гео избыточное резервное копирование — это восстановленный ресурс, использующий файлы данных из отдельного географического расположения.</span><span class="sxs-lookup"><span data-stu-id="9b2d9-109">A geo-redundant backup is a restorable resource using data files from a separate geographic location.</span></span>
<span data-ttu-id="9b2d9-110">Вы можете Geo-Restore резервную копию в случае регионального простоя, чтобы восстановить пул SQL в новом регионе.</span><span class="sxs-lookup"><span data-stu-id="9b2d9-110">You can use Geo-Restore to restore a geo-redundant backup in the event of a regional outage to recover your Sql Pool to a new region.</span></span>

## <span data-ttu-id="9b2d9-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9b2d9-111">EXAMPLES</span></span>

### <span data-ttu-id="9b2d9-112">Пример 1. Получить указанную геопроибытную резервную копию</span><span class="sxs-lookup"><span data-stu-id="9b2d9-112">Example 1: Get a specified geo-redundant backup</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolGeoBackup -ResourceGroupName ContosoResourceGroup -WorkspaceName "ContosoWorkspace" -Name "ContosoSqlPool"
```
<span data-ttu-id="9b2d9-113">Он извлекает геоархивную резервную копию для SQL-пула.</span><span class="sxs-lookup"><span data-stu-id="9b2d9-113">The cmdlet retrieves Geo Backup for a sql pool.</span></span>

### <span data-ttu-id="9b2d9-114">Пример 2. Получите все гео избыточные резервные копии в рабочей области</span><span class="sxs-lookup"><span data-stu-id="9b2d9-114">Example 2: Get all geo-redundant backups on a workspace</span></span>
```
PS C:\>Get-AzSynapseSqlPoolGeoBackup -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```
<span data-ttu-id="9b2d9-115">Эта команда получает все доступные гео избыточные резервные копии в указанной рабочей области.</span><span class="sxs-lookup"><span data-stu-id="9b2d9-115">This command gets all available geo-redundant backups on a specified workspace.</span></span>

### <span data-ttu-id="9b2d9-116">Пример 3. Получите все гео избыточные резервные копии в рабочей области с помощью фильтрации</span><span class="sxs-lookup"><span data-stu-id="9b2d9-116">Example 3: Get all geo-redundant backups on a workspace using filtering</span></span>
```
PS C:\>Get-AzSynapseSqlPoolGeoBackup -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -Name "Contoso*"
```
<span data-ttu-id="9b2d9-117">Эта команда получает все доступные гео избыточные резервные копии в указанной рабочей области, которая начинается с Contoso.</span><span class="sxs-lookup"><span data-stu-id="9b2d9-117">This command gets all available geo-redundant backups on a specified workspace that start with "Contoso".</span></span>

## <span data-ttu-id="9b2d9-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9b2d9-118">PARAMETERS</span></span>

### <span data-ttu-id="9b2d9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b2d9-119">-DefaultProfile</span></span>
<span data-ttu-id="9b2d9-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9b2d9-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b2d9-121">-Name</span><span class="sxs-lookup"><span data-stu-id="9b2d9-121">-Name</span></span>
<span data-ttu-id="9b2d9-122">Пул SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="9b2d9-122">The Synapse Sql pool.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: The Synapse Sql pool.

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b2d9-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9b2d9-123">-ResourceId</span></span>
<span data-ttu-id="9b2d9-124">Ввести ИД геоархивации пула Sql.</span><span class="sxs-lookup"><span data-stu-id="9b2d9-124">Input a Sql Pool Geo Backup Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: SqlPoolGeoBackupResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b2d9-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b2d9-125">-ResourceGroupName</span></span>
<span data-ttu-id="9b2d9-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9b2d9-126">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b2d9-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="9b2d9-127">-WorkspaceName</span></span>
<span data-ttu-id="9b2d9-128">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="9b2d9-128">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b2d9-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b2d9-129">CommonParameters</span></span>
<span data-ttu-id="9b2d9-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b2d9-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b2d9-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9b2d9-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b2d9-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9b2d9-132">INPUTS</span></span>

### <span data-ttu-id="9b2d9-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="9b2d9-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="9b2d9-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseResourceGroup</span><span class="sxs-lookup"><span data-stu-id="9b2d9-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseResourceGroup</span></span>

## <span data-ttu-id="9b2d9-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9b2d9-135">OUTPUTS</span></span>

### <span data-ttu-id="9b2d9-136">Microsoft.Azure.Commands.Synapse.Models.PSBackupModel</span><span class="sxs-lookup"><span data-stu-id="9b2d9-136">Microsoft.Azure.Commands.Synapse.Models.PSBackupModel</span></span>

## <span data-ttu-id="9b2d9-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9b2d9-137">NOTES</span></span>

## <span data-ttu-id="9b2d9-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9b2d9-138">RELATED LINKS</span></span>
