---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 52664E45-7EAB-41C9-BF78-304F10BFC51A
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlservercommunicationlink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerCommunicationLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerCommunicationLink.md
ms.openlocfilehash: 282ef9f77f5902d698353528b10e154eb7fd86ef
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100212481"
---
# <span data-ttu-id="67d12-101">New-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="67d12-101">New-AzSqlServerCommunicationLink</span></span>

## <span data-ttu-id="67d12-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67d12-102">SYNOPSIS</span></span>
<span data-ttu-id="67d12-103">Создает связь для эластичных транзакций базы данных между SQL базами данных.</span><span class="sxs-lookup"><span data-stu-id="67d12-103">Creates a communication link for elastic database transactions between two SQL Database servers.</span></span>

## <span data-ttu-id="67d12-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="67d12-104">SYNTAX</span></span>

```
New-AzSqlServerCommunicationLink -LinkName <String> -PartnerServer <String> [-AsJob] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="67d12-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="67d12-105">DESCRIPTION</span></span>
<span data-ttu-id="67d12-106">Командалет **New-AzSqlServerCommunicationLink** создает связь для передачи данных на эластичные транзакции между двумя логическими серверами в базе данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="67d12-106">The **New-AzSqlServerCommunicationLink** cmdlet creates a communication link for elastic database transactions between two logical servers in Azure SQL Database.</span></span>
<span data-ttu-id="67d12-107">Эластичные транзакции базы данных могут охватывать базы данных на любом из сопряженных серверов.</span><span class="sxs-lookup"><span data-stu-id="67d12-107">Elastic database transactions can span databases in either of the paired servers.</span></span>
<span data-ttu-id="67d12-108">На сервере можно создать несколько ссылок.</span><span class="sxs-lookup"><span data-stu-id="67d12-108">You can create more than one link on a server.</span></span>
<span data-ttu-id="67d12-109">Таким образом, эластичные транзакции базы данных могут охватывать большое количество серверов.</span><span class="sxs-lookup"><span data-stu-id="67d12-109">Therefore, elastic database transactions can span across a larger number of servers.</span></span>

## <span data-ttu-id="67d12-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="67d12-110">EXAMPLES</span></span>

### <span data-ttu-id="67d12-111">Пример 1. Создание связи</span><span class="sxs-lookup"><span data-stu-id="67d12-111">Example 1: Create a communication link</span></span>
```
PS C:\>New-AzSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17" -LinkName "Link01" -PartnerServer "ContosoServer02"
```

<span data-ttu-id="67d12-112">Эта команда создает ссылку "Ссылка01" между ContosoServer17 и ContosoServer02.</span><span class="sxs-lookup"><span data-stu-id="67d12-112">This command creates a link named Link01 between ContosoServer17 and ContosoServer02.</span></span>

## <span data-ttu-id="67d12-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="67d12-113">PARAMETERS</span></span>

### <span data-ttu-id="67d12-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="67d12-114">-AsJob</span></span>
<span data-ttu-id="67d12-115">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="67d12-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="67d12-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67d12-116">-DefaultProfile</span></span>
<span data-ttu-id="67d12-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="67d12-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="67d12-118">-LinkName</span><span class="sxs-lookup"><span data-stu-id="67d12-118">-LinkName</span></span>
<span data-ttu-id="67d12-119">Указывает имя серверной связи, которую создает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="67d12-119">Specifies the name of the server communication link that this cmdlet creates.</span></span>

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

### <span data-ttu-id="67d12-120">-PartnerServer</span><span class="sxs-lookup"><span data-stu-id="67d12-120">-PartnerServer</span></span>
<span data-ttu-id="67d12-121">Указывает имя другого сервера, который принимает участие в этой связи.</span><span class="sxs-lookup"><span data-stu-id="67d12-121">Specifies the name of the other server that takes part in this communication link.</span></span>

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

### <span data-ttu-id="67d12-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67d12-122">-ResourceGroupName</span></span>
<span data-ttu-id="67d12-123">Имя группы ресурсов, к которой принадлежит сервер, указанный параметром *ServerName.*</span><span class="sxs-lookup"><span data-stu-id="67d12-123">Specifies the name of the resource group to which the server specified by the *ServerName* parameter belongs.</span></span>

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

### <span data-ttu-id="67d12-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="67d12-124">-ServerName</span></span>
<span data-ttu-id="67d12-125">Указывает имя сервера, на котором этот cmdlet настраивает связь.</span><span class="sxs-lookup"><span data-stu-id="67d12-125">Specifies the name of the server on which this cmdlet sets up the communication link.</span></span>

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

### <span data-ttu-id="67d12-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="67d12-126">-Confirm</span></span>
<span data-ttu-id="67d12-127">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="67d12-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67d12-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67d12-128">-WhatIf</span></span>
<span data-ttu-id="67d12-129">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="67d12-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="67d12-130">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="67d12-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67d12-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67d12-131">CommonParameters</span></span>
<span data-ttu-id="67d12-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67d12-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67d12-133">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="67d12-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67d12-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="67d12-134">INPUTS</span></span>

### <span data-ttu-id="67d12-135">System.String</span><span class="sxs-lookup"><span data-stu-id="67d12-135">System.String</span></span>

## <span data-ttu-id="67d12-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="67d12-136">OUTPUTS</span></span>

### <span data-ttu-id="67d12-137">Microsoft.Azure.Commands.Sql.ServerCommunicationLink.Model.AzureSqlServerCommunicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="67d12-137">Microsoft.Azure.Commands.Sql.ServerCommunicationLink.Model.AzureSqlServerCommunicationLinkModel</span></span>

## <span data-ttu-id="67d12-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="67d12-138">NOTES</span></span>
* <span data-ttu-id="67d12-139">Ключевые слова: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span><span class="sxs-lookup"><span data-stu-id="67d12-139">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="67d12-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="67d12-140">RELATED LINKS</span></span>

[<span data-ttu-id="67d12-141">Get-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="67d12-141">Get-AzSqlServerCommunicationLink</span></span>](./Get-AzSqlServerCommunicationLink.md)

[<span data-ttu-id="67d12-142">Remove-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="67d12-142">Remove-AzSqlServerCommunicationLink</span></span>](./Remove-AzSqlServerCommunicationLink.md)

[<span data-ttu-id="67d12-143">SQL базы данных</span><span class="sxs-lookup"><span data-stu-id="67d12-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
