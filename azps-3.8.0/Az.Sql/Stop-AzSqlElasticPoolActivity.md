---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/stop-azsqlelasticpoolactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlElasticPoolActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlElasticPoolActivity.md
ms.openlocfilehash: dc1dffd84a95bd9cffac1dbafb5183d56e0b7c52
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93912472"
---
# <span data-ttu-id="86d53-101">Stop-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="86d53-101">Stop-AzSqlElasticPoolActivity</span></span>

## <span data-ttu-id="86d53-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="86d53-102">SYNOPSIS</span></span>
<span data-ttu-id="86d53-103">Отменяет асинхронную операцию обновления в пуле эластичных БД.</span><span class="sxs-lookup"><span data-stu-id="86d53-103">Cancels the asynchronous update operation on an elastic pool.</span></span>

## <span data-ttu-id="86d53-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="86d53-104">SYNTAX</span></span>

```
Stop-AzSqlElasticPoolActivity [-PassThru] [-ServerName] <String> [-ElasticPoolName] <String>
 [-OperationId <Guid>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="86d53-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="86d53-105">DESCRIPTION</span></span>
<span data-ttu-id="86d53-106">Командлет **Stop-AzSqlElasticPoolActivity** отменяет асинхронную операцию обновления в пуле эластичных БД.</span><span class="sxs-lookup"><span data-stu-id="86d53-106">The **Stop-AzSqlElasticPoolActivity** cmdlet cancels the asynchronous update operation on an elastic pool.</span></span>

## <span data-ttu-id="86d53-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="86d53-107">EXAMPLES</span></span>

### <span data-ttu-id="86d53-108">Пример 1: Отмена асинхронной операции обновления для пула эластичных БД</span><span class="sxs-lookup"><span data-stu-id="86d53-108">Example 1: Cancel the asynchronous update operation on an elastic pool</span></span>
```
PS C:\> Stop-AzSqlElasticPoolActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -OperationId af97005d-9243-4f8a-844e-402d1cc855f5

OperationId     : af97005d-9243-4f8a-844e-402d1cc855f5
ServerName      : Server01
DatabaseName    : ElasticPool01
State           : CANCELLED
Operation       : UpdateLogicalElasticPool
ErrorCode       :
ErrorMessage    :
ErrorSeverity   :
StartTime       : 10/15/2017 02:49:42 PM
EndTime         : 10/15/2017 02:49:43 PM
PercentComplete :
```

<span data-ttu-id="86d53-109">Эта команда отменяет операцию асинхронных обновлений в пуле эластичных БД.</span><span class="sxs-lookup"><span data-stu-id="86d53-109">This command cancels the asynchronous updates operation on the elastic pool.</span></span>

## <span data-ttu-id="86d53-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="86d53-110">PARAMETERS</span></span>

### <span data-ttu-id="86d53-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86d53-111">-DefaultProfile</span></span>
<span data-ttu-id="86d53-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="86d53-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="86d53-113">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="86d53-113">-ElasticPoolName</span></span>
<span data-ttu-id="86d53-114">Имя пула эластичных БД SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="86d53-114">The name of the Azure SQL Elastic Pool.</span></span>

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

### <span data-ttu-id="86d53-115">-С идентификатором</span><span class="sxs-lookup"><span data-stu-id="86d53-115">-OperationId</span></span>
<span data-ttu-id="86d53-116">ИДЕНТИФИКАТОР операции, которую требуется извлечь.</span><span class="sxs-lookup"><span data-stu-id="86d53-116">The ID of the operation to retrieve.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86d53-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="86d53-117">-PassThru</span></span>
<span data-ttu-id="86d53-118">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="86d53-118">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86d53-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86d53-119">-ResourceGroupName</span></span>
<span data-ttu-id="86d53-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="86d53-120">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86d53-121">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="86d53-121">-ServerName</span></span>
<span data-ttu-id="86d53-122">Имя сервера Azure SQL Server, в котором находится пул эластичных БД.</span><span class="sxs-lookup"><span data-stu-id="86d53-122">The name of the Azure SQL Server the Elastic Pool is in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86d53-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="86d53-123">-Confirm</span></span>
<span data-ttu-id="86d53-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="86d53-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86d53-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86d53-125">-WhatIf</span></span>
<span data-ttu-id="86d53-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="86d53-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="86d53-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="86d53-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86d53-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86d53-128">CommonParameters</span></span>
<span data-ttu-id="86d53-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="86d53-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86d53-130">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="86d53-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86d53-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="86d53-131">INPUTS</span></span>

### <span data-ttu-id="86d53-132">System. String</span><span class="sxs-lookup"><span data-stu-id="86d53-132">System.String</span></span>

### <span data-ttu-id="86d53-133">System. Nullable "1 [[System. GUID, System. Private. CoreLib, Version = 4.0.0.0, культура = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="86d53-133">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="86d53-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="86d53-134">OUTPUTS</span></span>

### <span data-ttu-id="86d53-135">Microsoft. Azure. Commands. SQL. ElasticPool. Model. AzureSqlElasticPoolActivityModel</span><span class="sxs-lookup"><span data-stu-id="86d53-135">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolActivityModel</span></span>

## <span data-ttu-id="86d53-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="86d53-136">NOTES</span></span>

## <span data-ttu-id="86d53-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="86d53-137">RELATED LINKS</span></span>
