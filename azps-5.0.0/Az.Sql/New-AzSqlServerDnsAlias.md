---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlserverdnsalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerDnsAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerDnsAlias.md
ms.openlocfilehash: 66f8c3acc178a922868177200e6d4f1f8f50931f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246657"
---
# <span data-ttu-id="25454-101">New-AzSqlServerDnsAlias</span><span class="sxs-lookup"><span data-stu-id="25454-101">New-AzSqlServerDnsAlias</span></span>

## <span data-ttu-id="25454-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="25454-102">SYNOPSIS</span></span>
<span data-ttu-id="25454-103">Эта команда создает новый DNS-псевдоним для Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="25454-103">This command creates a new Azure SQL Server DNS Alias.</span></span>

## <span data-ttu-id="25454-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="25454-104">SYNTAX</span></span>

```
New-AzSqlServerDnsAlias -Name <String> [-AsJob] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="25454-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="25454-105">DESCRIPTION</span></span>
<span data-ttu-id="25454-106">Создает новый DNS-псевдоним Azure SQL Server, указывающий на указанный сервер.</span><span class="sxs-lookup"><span data-stu-id="25454-106">Creates new Azure SQL Server DNS Alias that is pointing to specified server.</span></span>

## <span data-ttu-id="25454-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="25454-107">EXAMPLES</span></span>

### <span data-ttu-id="25454-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="25454-108">Example 1</span></span>
```
PS C:\> $serverDNSAlias = New-AzSqlServerDnsAlias -ResourceGroupName rg -ServerName serverName -DnsAliasName aliasName

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
```

<span data-ttu-id="25454-109">Эта команда создает псевдоним DNS для Azure SQL Server с именем aliasName, указывающим на сервер serverName.</span><span class="sxs-lookup"><span data-stu-id="25454-109">This command creates Azure SQL Server DNS Alias with the name aliasName that is pointing to server serverName</span></span>

## <span data-ttu-id="25454-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="25454-110">PARAMETERS</span></span>

### <span data-ttu-id="25454-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="25454-111">-AsJob</span></span>
<span data-ttu-id="25454-112">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="25454-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="25454-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25454-113">-DefaultProfile</span></span>
<span data-ttu-id="25454-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="25454-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="25454-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="25454-115">-Name</span></span>
<span data-ttu-id="25454-116">Имя псевдонима DNS для Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="25454-116">The Azure Sql Server Dns Alias name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DnsAliasName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25454-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25454-117">-ResourceGroupName</span></span>
<span data-ttu-id="25454-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="25454-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="25454-119">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="25454-119">-ServerName</span></span>
<span data-ttu-id="25454-120">Имя сервера Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="25454-120">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="25454-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="25454-121">-Confirm</span></span>
<span data-ttu-id="25454-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="25454-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25454-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25454-123">-WhatIf</span></span>
<span data-ttu-id="25454-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="25454-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="25454-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="25454-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25454-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25454-126">CommonParameters</span></span>
<span data-ttu-id="25454-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="25454-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25454-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="25454-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25454-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="25454-129">INPUTS</span></span>

### <span data-ttu-id="25454-130">System. String</span><span class="sxs-lookup"><span data-stu-id="25454-130">System.String</span></span>

## <span data-ttu-id="25454-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="25454-131">OUTPUTS</span></span>

### <span data-ttu-id="25454-132">Microsoft. Azure. Commands. SQL. ServerDnsAlias. Model. AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="25454-132">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="25454-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="25454-133">NOTES</span></span>

## <span data-ttu-id="25454-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="25454-134">RELATED LINKS</span></span>
