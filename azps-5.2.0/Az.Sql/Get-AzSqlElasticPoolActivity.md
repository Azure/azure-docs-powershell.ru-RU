---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 0DB0B08A-F948-4F6E-9CF0-2FB5DD5064D3
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlelasticpoolactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolActivity.md
ms.openlocfilehash: 2e0768b14337f4504df1e6cdf9565533584e0339
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98411164"
---
# <span data-ttu-id="a72d0-101">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="a72d0-101">Get-AzSqlElasticPoolActivity</span></span>

## <span data-ttu-id="a72d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a72d0-102">SYNOPSIS</span></span>
<span data-ttu-id="a72d0-103">Возвращает состояние операций в эластичном пуле.</span><span class="sxs-lookup"><span data-stu-id="a72d0-103">Gets the status of operations on an elastic pool.</span></span>

## <span data-ttu-id="a72d0-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a72d0-104">SYNTAX</span></span>

```
Get-AzSqlElasticPoolActivity [-ServerName] <String> [-ElasticPoolName] <String> [-OperationId <Guid>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a72d0-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a72d0-105">DESCRIPTION</span></span>
<span data-ttu-id="a72d0-106">Cmdlet **Get-AzSqlElasticPoolActivity** получает состояние операций в эластичном пуле для базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="a72d0-106">The **Get-AzSqlElasticPoolActivity** cmdlet gets the status of operations on an elastic pool for an Azure SQL Database.</span></span>
<span data-ttu-id="a72d0-107">Вы увидите состояние обновлений для создания пула и конфигурации.</span><span class="sxs-lookup"><span data-stu-id="a72d0-107">You can see the status of both pool creation and configuration updates.</span></span>

## <span data-ttu-id="a72d0-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a72d0-108">EXAMPLES</span></span>

### <span data-ttu-id="a72d0-109">Пример 1. Просмотр состояния операций для эластичного пула</span><span class="sxs-lookup"><span data-stu-id="a72d0-109">Example 1: Get the status of operations for an elastic pool</span></span>
```
PS C:\>Get-AzSqlElasticPoolActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="a72d0-110">Эта команда получает состояние операций для эластичного пула с именем "Эластичный пул01".</span><span class="sxs-lookup"><span data-stu-id="a72d0-110">This command gets the status of the operations for the elastic pool named ElasticPool01.</span></span>

## <span data-ttu-id="a72d0-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a72d0-111">PARAMETERS</span></span>

### <span data-ttu-id="a72d0-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a72d0-112">-DefaultProfile</span></span>
<span data-ttu-id="a72d0-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="a72d0-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a72d0-114">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="a72d0-114">-ElasticPoolName</span></span>
<span data-ttu-id="a72d0-115">Определяет имя эластичного пула.</span><span class="sxs-lookup"><span data-stu-id="a72d0-115">Specifies the name of an elastic pool.</span></span>

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

### <span data-ttu-id="a72d0-116">-OperationId</span><span class="sxs-lookup"><span data-stu-id="a72d0-116">-OperationId</span></span>
<span data-ttu-id="a72d0-117">ИД извлекаемой операции.</span><span class="sxs-lookup"><span data-stu-id="a72d0-117">The ID of the operation to retrieve.</span></span>

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

### <span data-ttu-id="a72d0-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a72d0-118">-ResourceGroupName</span></span>
<span data-ttu-id="a72d0-119">Указывает имя группы ресурсов, которой назначено эластичное пул.</span><span class="sxs-lookup"><span data-stu-id="a72d0-119">Specifies the name of a resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="a72d0-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a72d0-120">-ServerName</span></span>
<span data-ttu-id="a72d0-121">Имя сервера, который содержит эластичный пул.</span><span class="sxs-lookup"><span data-stu-id="a72d0-121">Specifies the name of a server that contains an elastic pool.</span></span>

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

### <span data-ttu-id="a72d0-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a72d0-122">-Confirm</span></span>
<span data-ttu-id="a72d0-123">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a72d0-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a72d0-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a72d0-124">-WhatIf</span></span>
<span data-ttu-id="a72d0-125">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a72d0-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a72d0-126">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="a72d0-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a72d0-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a72d0-127">CommonParameters</span></span>
<span data-ttu-id="a72d0-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a72d0-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a72d0-129">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a72d0-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a72d0-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a72d0-130">INPUTS</span></span>

### <span data-ttu-id="a72d0-131">System.String</span><span class="sxs-lookup"><span data-stu-id="a72d0-131">System.String</span></span>

### <span data-ttu-id="a72d0-132">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="a72d0-132">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="a72d0-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a72d0-133">OUTPUTS</span></span>

### <span data-ttu-id="a72d0-134">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolActivityModel</span><span class="sxs-lookup"><span data-stu-id="a72d0-134">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolActivityModel</span></span>

## <span data-ttu-id="a72d0-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a72d0-135">NOTES</span></span>

## <span data-ttu-id="a72d0-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a72d0-136">RELATED LINKS</span></span>

[<span data-ttu-id="a72d0-137">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="a72d0-137">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="a72d0-138">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="a72d0-138">Get-AzSqlElasticPoolDatabase</span></span>](./Get-AzSqlElasticPoolDatabase.md)

[<span data-ttu-id="a72d0-139">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="a72d0-139">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="a72d0-140">Remove-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="a72d0-140">Remove-AzSqlElasticPool</span></span>](./Remove-AzSqlElasticPool.md)

[<span data-ttu-id="a72d0-141">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="a72d0-141">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)


