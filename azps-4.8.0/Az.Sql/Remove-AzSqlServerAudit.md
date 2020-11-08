---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Remove-AzSqlServerAudit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerAudit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerAudit.md
ms.openlocfilehash: ce9bf1a2c7b72e6da92c17e343a993294f8e335d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243223"
---
# <span data-ttu-id="48327-101">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="48327-101">Remove-AzSqlServerAudit</span></span>

## <span data-ttu-id="48327-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="48327-102">SYNOPSIS</span></span>
<span data-ttu-id="48327-103">Удаляет параметры аудита для Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="48327-103">Removes the auditing settings of an Azure SQL server.</span></span>

## <span data-ttu-id="48327-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="48327-104">SYNTAX</span></span>

### <span data-ttu-id="48327-105">ServerParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="48327-105">ServerParameterSet (Default)</span></span>
```
Remove-AzSqlServerAudit [-ResourceGroupName] <String> [-ServerName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48327-106">ServerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="48327-106">ServerObjectParameterSet</span></span>
```
Remove-AzSqlServerAudit -ServerObject <AzureSqlServerModel> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="48327-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="48327-107">DESCRIPTION</span></span>
<span data-ttu-id="48327-108">Командлет **Remove-AzSqlServerAudit** удаляет параметры аудита для Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="48327-108">The **Remove-AzSqlServerAudit** cmdlet removes the auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="48327-109">Укажите параметры *ResourceGroupName* и *ServerName* для идентификации сервера.</span><span class="sxs-lookup"><span data-stu-id="48327-109">Specify the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>

## <span data-ttu-id="48327-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="48327-110">EXAMPLES</span></span>

### <span data-ttu-id="48327-111">Пример 1: удаление параметров аудита для Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="48327-111">Example 1: Remove the auditing settings of an Azure SQL server</span></span>
```
PS C:\>Remove-AzSqlServerAudit -ResourceGroupName "resourcegroup01" -ServerName "server01"
```

### <span data-ttu-id="48327-112">Пример 2: удаление с помощью конвейера параметры аудита для Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="48327-112">Example 2: Remove, through pipeline, the auditing settings of an Azure SQL server</span></span>
```
PS C:\> Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Remove-AzSqlServerAudit
```

## <span data-ttu-id="48327-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="48327-113">PARAMETERS</span></span>

### <span data-ttu-id="48327-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="48327-114">-AsJob</span></span>
<span data-ttu-id="48327-115">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="48327-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="48327-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48327-116">-DefaultProfile</span></span>
<span data-ttu-id="48327-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="48327-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="48327-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48327-118">-ResourceGroupName</span></span>
<span data-ttu-id="48327-119">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="48327-119">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48327-120">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="48327-120">-ServerName</span></span>
<span data-ttu-id="48327-121">Имя сервера SQL Server.</span><span class="sxs-lookup"><span data-stu-id="48327-121">SQL server name.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48327-122">-ServerObject</span><span class="sxs-lookup"><span data-stu-id="48327-122">-ServerObject</span></span>
<span data-ttu-id="48327-123">Объект сервера для управления политикой аудита.</span><span class="sxs-lookup"><span data-stu-id="48327-123">The server object to manage its audit policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel
Parameter Sets: ServerObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="48327-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="48327-124">-Confirm</span></span>
<span data-ttu-id="48327-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="48327-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48327-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48327-126">-WhatIf</span></span>
<span data-ttu-id="48327-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="48327-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="48327-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="48327-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="48327-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48327-129">CommonParameters</span></span>
<span data-ttu-id="48327-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="48327-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48327-131">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="48327-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48327-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="48327-132">INPUTS</span></span>

### <span data-ttu-id="48327-133">System. String</span><span class="sxs-lookup"><span data-stu-id="48327-133">System.String</span></span>

### <span data-ttu-id="48327-134">Microsoft. Azure. Commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="48327-134">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="48327-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="48327-135">OUTPUTS</span></span>

### <span data-ttu-id="48327-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="48327-136">System.Boolean</span></span>

## <span data-ttu-id="48327-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="48327-137">NOTES</span></span>

## <span data-ttu-id="48327-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="48327-138">RELATED LINKS</span></span>