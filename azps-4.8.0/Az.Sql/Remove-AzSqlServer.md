---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 068D70EF-39D1-4199-BD74-0EC266DF7072
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServer.md
ms.openlocfilehash: 670b3e6ec71a768fe40bbcf542440db5ec685b2f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235775"
---
# <span data-ttu-id="baa47-101">Remove-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="baa47-101">Remove-AzSqlServer</span></span>

## <span data-ttu-id="baa47-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="baa47-102">SYNOPSIS</span></span>
<span data-ttu-id="baa47-103">Удаляет сервер базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="baa47-103">Removes an Azure SQL Database server.</span></span>

## <span data-ttu-id="baa47-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="baa47-104">SYNTAX</span></span>

```
Remove-AzSqlServer [-ServerName] <String> [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="baa47-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="baa47-105">DESCRIPTION</span></span>
<span data-ttu-id="baa47-106">Командлет **Remove-AzSqlServer** удаляет сервер базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="baa47-106">The **Remove-AzSqlServer** cmdlet removes an Azure SQL Database server.</span></span>
<span data-ttu-id="baa47-107">Операция удаления является асинхронной и может занять некоторое время, поэтому перед выполнением каких – либо дополнительных операций, зависящих от того, что сервер удаляется, необходимо проверить, не завершилась ли операция.</span><span class="sxs-lookup"><span data-stu-id="baa47-107">The delete operation is asynchronous and may take some time, so verify the operation is finished before performing any additional operations that depend on the server being completely deleted.</span></span>
<span data-ttu-id="baa47-108">Например, вам нужно создать новый сервер с тем же именем.</span><span class="sxs-lookup"><span data-stu-id="baa47-108">For instance, you need to create a new server that uses the same name.</span></span>

## <span data-ttu-id="baa47-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="baa47-109">EXAMPLES</span></span>

### <span data-ttu-id="baa47-110">Пример 1: Удаление сервера</span><span class="sxs-lookup"><span data-stu-id="baa47-110">Example 1: Remove a server</span></span>
```
PS C:\>Remove-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="baa47-111">Эта команда удаляет сервер базы данных SQL Azure с именем Server01.</span><span class="sxs-lookup"><span data-stu-id="baa47-111">This command removes the Azure SQL Database server named Server01.</span></span>

## <span data-ttu-id="baa47-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="baa47-112">PARAMETERS</span></span>

### <span data-ttu-id="baa47-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="baa47-113">-DefaultProfile</span></span>
<span data-ttu-id="baa47-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="baa47-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="baa47-115">-Force</span><span class="sxs-lookup"><span data-stu-id="baa47-115">-Force</span></span>
<span data-ttu-id="baa47-116">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="baa47-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="baa47-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="baa47-117">-ResourceGroupName</span></span>
<span data-ttu-id="baa47-118">Указывает имя группы ресурсов, которой назначен сервер.</span><span class="sxs-lookup"><span data-stu-id="baa47-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="baa47-119">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="baa47-119">-ServerName</span></span>
<span data-ttu-id="baa47-120">Указывает имя сервера, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="baa47-120">Specifies the name of the server to remove.</span></span>

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

### <span data-ttu-id="baa47-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="baa47-121">-Confirm</span></span>
<span data-ttu-id="baa47-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="baa47-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="baa47-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="baa47-123">-WhatIf</span></span>
<span data-ttu-id="baa47-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="baa47-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="baa47-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="baa47-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="baa47-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="baa47-126">CommonParameters</span></span>
<span data-ttu-id="baa47-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="baa47-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="baa47-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="baa47-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="baa47-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="baa47-129">INPUTS</span></span>

### <span data-ttu-id="baa47-130">System. String</span><span class="sxs-lookup"><span data-stu-id="baa47-130">System.String</span></span>

## <span data-ttu-id="baa47-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="baa47-131">OUTPUTS</span></span>

### <span data-ttu-id="baa47-132">Microsoft. Azure. Commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="baa47-132">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="baa47-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="baa47-133">NOTES</span></span>

## <span data-ttu-id="baa47-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="baa47-134">RELATED LINKS</span></span>

[<span data-ttu-id="baa47-135">Get-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="baa47-135">Get-AzSqlServer</span></span>](./Get-AzSqlServer.md)

[<span data-ttu-id="baa47-136">New-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="baa47-136">New-AzSqlServer</span></span>](./New-AzSqlServer.md)

[<span data-ttu-id="baa47-137">Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="baa47-137">Set-AzSqlServer</span></span>](./Set-AzSqlServer.md)

[<span data-ttu-id="baa47-138">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="baa47-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


