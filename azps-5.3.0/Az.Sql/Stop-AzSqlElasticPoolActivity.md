---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/stop-azsqlelasticpoolactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlElasticPoolActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlElasticPoolActivity.md
ms.openlocfilehash: dc1dffd84a95bd9cffac1dbafb5183d56e0b7c52
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506615"
---
# <span data-ttu-id="f4003-101">Stop-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="f4003-101">Stop-AzSqlElasticPoolActivity</span></span>

## <span data-ttu-id="f4003-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f4003-102">SYNOPSIS</span></span>
<span data-ttu-id="f4003-103">Отмена асинхронного обновления для эластичного пула.</span><span class="sxs-lookup"><span data-stu-id="f4003-103">Cancels the asynchronous update operation on an elastic pool.</span></span>

## <span data-ttu-id="f4003-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f4003-104">SYNTAX</span></span>

```
Stop-AzSqlElasticPoolActivity [-PassThru] [-ServerName] <String> [-ElasticPoolName] <String>
 [-OperationId <Guid>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4003-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f4003-105">DESCRIPTION</span></span>
<span data-ttu-id="f4003-106">Cmdlet **Stop-AzSqlElasticPoolActivity** отменяет асинхронное обновление в эластичном пуле.</span><span class="sxs-lookup"><span data-stu-id="f4003-106">The **Stop-AzSqlElasticPoolActivity** cmdlet cancels the asynchronous update operation on an elastic pool.</span></span>

## <span data-ttu-id="f4003-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f4003-107">EXAMPLES</span></span>

### <span data-ttu-id="f4003-108">Пример 1. Отмена асинхронного обновления для эластичного пула</span><span class="sxs-lookup"><span data-stu-id="f4003-108">Example 1: Cancel the asynchronous update operation on an elastic pool</span></span>
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

<span data-ttu-id="f4003-109">Эта команда отменяет операцию асинхронного обновления для эластичного пула.</span><span class="sxs-lookup"><span data-stu-id="f4003-109">This command cancels the asynchronous updates operation on the elastic pool.</span></span>

## <span data-ttu-id="f4003-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f4003-110">PARAMETERS</span></span>

### <span data-ttu-id="f4003-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4003-111">-DefaultProfile</span></span>
<span data-ttu-id="f4003-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f4003-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4003-113">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="f4003-113">-ElasticPoolName</span></span>
<span data-ttu-id="f4003-114">Имя эластичного пула Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="f4003-114">The name of the Azure SQL Elastic Pool.</span></span>

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

### <span data-ttu-id="f4003-115">-OperationId</span><span class="sxs-lookup"><span data-stu-id="f4003-115">-OperationId</span></span>
<span data-ttu-id="f4003-116">ИД извлекаемой операции.</span><span class="sxs-lookup"><span data-stu-id="f4003-116">The ID of the operation to retrieve.</span></span>

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

### <span data-ttu-id="f4003-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f4003-117">-PassThru</span></span>
<span data-ttu-id="f4003-118">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="f4003-118">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="f4003-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4003-119">-ResourceGroupName</span></span>
<span data-ttu-id="f4003-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f4003-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="f4003-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f4003-121">-ServerName</span></span>
<span data-ttu-id="f4003-122">Имя Azure SQL Server есть в этом пуле.</span><span class="sxs-lookup"><span data-stu-id="f4003-122">The name of the Azure SQL Server the Elastic Pool is in.</span></span>

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

### <span data-ttu-id="f4003-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f4003-123">-Confirm</span></span>
<span data-ttu-id="f4003-124">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f4003-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4003-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4003-125">-WhatIf</span></span>
<span data-ttu-id="f4003-126">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f4003-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f4003-127">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="f4003-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4003-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4003-128">CommonParameters</span></span>
<span data-ttu-id="f4003-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4003-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4003-130">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f4003-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4003-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f4003-131">INPUTS</span></span>

### <span data-ttu-id="f4003-132">System.String</span><span class="sxs-lookup"><span data-stu-id="f4003-132">System.String</span></span>

### <span data-ttu-id="f4003-133">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="f4003-133">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="f4003-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f4003-134">OUTPUTS</span></span>

### <span data-ttu-id="f4003-135">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolActivityModel</span><span class="sxs-lookup"><span data-stu-id="f4003-135">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolActivityModel</span></span>

## <span data-ttu-id="f4003-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f4003-136">NOTES</span></span>

## <span data-ttu-id="f4003-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f4003-137">RELATED LINKS</span></span>
