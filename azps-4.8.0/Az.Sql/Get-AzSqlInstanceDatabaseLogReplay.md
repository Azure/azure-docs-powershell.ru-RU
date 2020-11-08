---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Get-AzSqlInstanceDatabaseLogReplay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseLogReplay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseLogReplay.md
ms.openlocfilehash: 7e37dcceb45370e4956fb59912a50a501fe271c1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243249"
---
# <span data-ttu-id="84d06-101">Get-AzSqlInstanceDatabaseLogReplay</span><span class="sxs-lookup"><span data-stu-id="84d06-101">Get-AzSqlInstanceDatabaseLogReplay</span></span>

## <span data-ttu-id="84d06-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="84d06-102">SYNOPSIS</span></span>
<span data-ttu-id="84d06-103">Возвращает состояние службы воспроизведения журнала.</span><span class="sxs-lookup"><span data-stu-id="84d06-103">Gets the Log Replay service status.</span></span>

## <span data-ttu-id="84d06-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="84d06-104">SYNTAX</span></span>

```
Get-AzSqlInstanceDatabaseLogReplay [[-Name] <String>] [-InstanceName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="84d06-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="84d06-105">DESCRIPTION</span></span>
<span data-ttu-id="84d06-106">Командлет **Get-AzSqlInstanceDatabaseLogReplay** получает состояние службы воспроизведения журнала для указанной базы данных.</span><span class="sxs-lookup"><span data-stu-id="84d06-106">The **Get-AzSqlInstanceDatabaseLogReplay** cmdlet gets the Log Replay service status on the given database.</span></span>

## <span data-ttu-id="84d06-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="84d06-107">EXAMPLES</span></span>

### <span data-ttu-id="84d06-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="84d06-108">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseLogReplay -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" -Name "ManagedDatabaseName"
```

<span data-ttu-id="84d06-109">Эта команда будет получать состояние службы воспроизведения журнала для указанной базы данных.</span><span class="sxs-lookup"><span data-stu-id="84d06-109">This command will get log replay service status on the given database.</span></span>

## <span data-ttu-id="84d06-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="84d06-110">PARAMETERS</span></span>

### <span data-ttu-id="84d06-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84d06-111">-DefaultProfile</span></span>
<span data-ttu-id="84d06-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="84d06-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="84d06-113">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="84d06-113">-InstanceName</span></span>
<span data-ttu-id="84d06-114">Имя экземпляра.</span><span class="sxs-lookup"><span data-stu-id="84d06-114">The name of the instance.</span></span>

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

### <span data-ttu-id="84d06-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="84d06-115">-Name</span></span>
<span data-ttu-id="84d06-116">Имя извлекаемой базы данных экземпляра.</span><span class="sxs-lookup"><span data-stu-id="84d06-116">The name of the instance database to retrieve.</span></span>

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

### <span data-ttu-id="84d06-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84d06-117">-ResourceGroupName</span></span>
<span data-ttu-id="84d06-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="84d06-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="84d06-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84d06-119">CommonParameters</span></span>
<span data-ttu-id="84d06-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="84d06-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84d06-121">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="84d06-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84d06-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="84d06-122">INPUTS</span></span>

### <span data-ttu-id="84d06-123">System. String</span><span class="sxs-lookup"><span data-stu-id="84d06-123">System.String</span></span>

## <span data-ttu-id="84d06-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="84d06-124">OUTPUTS</span></span>

### <span data-ttu-id="84d06-125">Microsoft. Azure. Commands. SQL. ManagedDatabase. Model. AzureSqlManagedDatabaseRestoreDetailsResultModel</span><span class="sxs-lookup"><span data-stu-id="84d06-125">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseRestoreDetailsResultModel</span></span>

## <span data-ttu-id="84d06-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="84d06-126">NOTES</span></span>

## <span data-ttu-id="84d06-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="84d06-127">RELATED LINKS</span></span>
