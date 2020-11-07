---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 068D70EF-39D1-4199-BD74-0EC266DF7072
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServer.md
ms.openlocfilehash: 52e0d37777b349744cf82f891fe8f711758f5a64
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93728839"
---
# <span data-ttu-id="1a7c2-101">Remove-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="1a7c2-101">Remove-AzSqlServer</span></span>

## <span data-ttu-id="1a7c2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1a7c2-102">SYNOPSIS</span></span>
<span data-ttu-id="1a7c2-103">Удаляет сервер базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="1a7c2-103">Removes an Azure SQL Database server.</span></span>

## <span data-ttu-id="1a7c2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1a7c2-104">SYNTAX</span></span>

```
Remove-AzSqlServer [-ServerName] <String> [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1a7c2-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1a7c2-105">DESCRIPTION</span></span>
<span data-ttu-id="1a7c2-106">Командлет **Remove-AzSqlServer** удаляет сервер базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="1a7c2-106">The **Remove-AzSqlServer** cmdlet removes an Azure SQL Database server.</span></span>
<span data-ttu-id="1a7c2-107">Операция удаления является асинхронной и может занять некоторое время, поэтому перед выполнением каких – либо дополнительных операций, зависящих от того, что сервер удаляется, необходимо проверить, не завершилась ли операция.</span><span class="sxs-lookup"><span data-stu-id="1a7c2-107">The delete operation is asynchronous and may take some time, so verify the operation is finished before performing any additional operations that depend on the server being completely deleted.</span></span>
<span data-ttu-id="1a7c2-108">Например, вам нужно создать новый сервер с тем же именем.</span><span class="sxs-lookup"><span data-stu-id="1a7c2-108">For instance, you need to create a new server that uses the same name.</span></span>

## <span data-ttu-id="1a7c2-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1a7c2-109">EXAMPLES</span></span>

### <span data-ttu-id="1a7c2-110">Пример 1: Удаление сервера</span><span class="sxs-lookup"><span data-stu-id="1a7c2-110">Example 1: Remove a server</span></span>
```
PS C:\>Remove-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="1a7c2-111">Эта команда удаляет сервер базы данных SQL Azure с именем Server01.</span><span class="sxs-lookup"><span data-stu-id="1a7c2-111">This command removes the Azure SQL Database server named Server01.</span></span>

## <span data-ttu-id="1a7c2-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1a7c2-112">PARAMETERS</span></span>

### <span data-ttu-id="1a7c2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a7c2-113">-DefaultProfile</span></span>
<span data-ttu-id="1a7c2-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="1a7c2-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1a7c2-115">-Force</span><span class="sxs-lookup"><span data-stu-id="1a7c2-115">-Force</span></span>
<span data-ttu-id="1a7c2-116">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="1a7c2-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1a7c2-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a7c2-117">-ResourceGroupName</span></span>
<span data-ttu-id="1a7c2-118">Указывает имя группы ресурсов, которой назначен сервер.</span><span class="sxs-lookup"><span data-stu-id="1a7c2-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="1a7c2-119">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="1a7c2-119">-ServerName</span></span>
<span data-ttu-id="1a7c2-120">Указывает имя сервера, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="1a7c2-120">Specifies the name of the server to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a7c2-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1a7c2-121">-Confirm</span></span>
<span data-ttu-id="1a7c2-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1a7c2-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a7c2-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a7c2-123">-WhatIf</span></span>
<span data-ttu-id="1a7c2-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="1a7c2-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1a7c2-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1a7c2-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a7c2-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a7c2-126">CommonParameters</span></span>
<span data-ttu-id="1a7c2-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1a7c2-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a7c2-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1a7c2-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a7c2-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1a7c2-129">INPUTS</span></span>

### <span data-ttu-id="1a7c2-130">System. String</span><span class="sxs-lookup"><span data-stu-id="1a7c2-130">System.String</span></span>

## <span data-ttu-id="1a7c2-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1a7c2-131">OUTPUTS</span></span>

### <span data-ttu-id="1a7c2-132">Microsoft. Azure. Commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="1a7c2-132">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="1a7c2-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="1a7c2-133">NOTES</span></span>

## <span data-ttu-id="1a7c2-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1a7c2-134">RELATED LINKS</span></span>

[<span data-ttu-id="1a7c2-135">Get-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="1a7c2-135">Get-AzSqlServer</span></span>](./Get-AzSqlServer.md)

[<span data-ttu-id="1a7c2-136">New-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="1a7c2-136">New-AzSqlServer</span></span>](./New-AzSqlServer.md)

[<span data-ttu-id="1a7c2-137">Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="1a7c2-137">Set-AzSqlServer</span></span>](./Set-AzSqlServer.md)

[<span data-ttu-id="1a7c2-138">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="1a7c2-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


