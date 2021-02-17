---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Get-AzSqlInstanceDatabaseLogReplay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseLogReplay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseLogReplay.md
ms.openlocfilehash: 7e37dcceb45370e4956fb59912a50a501fe271c1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100232633"
---
# <span data-ttu-id="4019f-101">Get-AzSqlInstanceDatabaseLogReplay</span><span class="sxs-lookup"><span data-stu-id="4019f-101">Get-AzSqlInstanceDatabaseLogReplay</span></span>

## <span data-ttu-id="4019f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4019f-102">SYNOPSIS</span></span>
<span data-ttu-id="4019f-103">Возвращает состояние службы воспроизведения журнала.</span><span class="sxs-lookup"><span data-stu-id="4019f-103">Gets the Log Replay service status.</span></span>

## <span data-ttu-id="4019f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4019f-104">SYNTAX</span></span>

```
Get-AzSqlInstanceDatabaseLogReplay [[-Name] <String>] [-InstanceName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4019f-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4019f-105">DESCRIPTION</span></span>
<span data-ttu-id="4019f-106">Чтобы получить состояние службы "Воспроизведение журнала" в данной базе данных, можно получить состояние службы **"Get-AzSqlInstanceDatabaseLogReplay".**</span><span class="sxs-lookup"><span data-stu-id="4019f-106">The **Get-AzSqlInstanceDatabaseLogReplay** cmdlet gets the Log Replay service status on the given database.</span></span>

## <span data-ttu-id="4019f-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4019f-107">EXAMPLES</span></span>

### <span data-ttu-id="4019f-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4019f-108">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseLogReplay -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" -Name "ManagedDatabaseName"
```

<span data-ttu-id="4019f-109">Эта команда будет получать состояние службы воспроизведения журнала в данной базе данных.</span><span class="sxs-lookup"><span data-stu-id="4019f-109">This command will get log replay service status on the given database.</span></span>

## <span data-ttu-id="4019f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4019f-110">PARAMETERS</span></span>

### <span data-ttu-id="4019f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4019f-111">-DefaultProfile</span></span>
<span data-ttu-id="4019f-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4019f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4019f-113">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="4019f-113">-InstanceName</span></span>
<span data-ttu-id="4019f-114">Имя экземпляра.</span><span class="sxs-lookup"><span data-stu-id="4019f-114">The name of the instance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ManagedInstanceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4019f-115">-Name</span><span class="sxs-lookup"><span data-stu-id="4019f-115">-Name</span></span>
<span data-ttu-id="4019f-116">Имя базы данных экземпляра, который нужно извлечь.</span><span class="sxs-lookup"><span data-stu-id="4019f-116">The name of the instance database to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: InstanceDatabaseName

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4019f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4019f-117">-ResourceGroupName</span></span>
<span data-ttu-id="4019f-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4019f-118">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4019f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4019f-119">CommonParameters</span></span>
<span data-ttu-id="4019f-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4019f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4019f-121">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4019f-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4019f-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4019f-122">INPUTS</span></span>

### <span data-ttu-id="4019f-123">System.String</span><span class="sxs-lookup"><span data-stu-id="4019f-123">System.String</span></span>

## <span data-ttu-id="4019f-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4019f-124">OUTPUTS</span></span>

### <span data-ttu-id="4019f-125">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseRestoreDetailsResultModel</span><span class="sxs-lookup"><span data-stu-id="4019f-125">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseRestoreDetailsResultModel</span></span>

## <span data-ttu-id="4019f-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4019f-126">NOTES</span></span>

## <span data-ttu-id="4019f-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4019f-127">RELATED LINKS</span></span>
