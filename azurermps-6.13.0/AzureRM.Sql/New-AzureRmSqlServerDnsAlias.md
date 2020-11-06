---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlserverdnsalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerDnsAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerDnsAlias.md
ms.openlocfilehash: 3ce18369645705f78722f7505c8dd1e46f2514b0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558231"
---
# <span data-ttu-id="88641-101">New-AzureRmSqlServerDnsAlias</span><span class="sxs-lookup"><span data-stu-id="88641-101">New-AzureRmSqlServerDnsAlias</span></span>

## <span data-ttu-id="88641-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="88641-102">SYNOPSIS</span></span>
<span data-ttu-id="88641-103">Эта команда создает новый DNS-псевдоним для Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="88641-103">This command creates a new Azure SQL Server DNS Alias.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="88641-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="88641-104">SYNTAX</span></span>

```
New-AzureRmSqlServerDnsAlias -Name <String> [-AsJob] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="88641-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="88641-105">DESCRIPTION</span></span>
<span data-ttu-id="88641-106">Создает новый DNS-псевдоним Azure SQL Server, указывающий на указанный сервер.</span><span class="sxs-lookup"><span data-stu-id="88641-106">Creates new Azure SQL Server DNS Alias that is pointing to specified server.</span></span>

## <span data-ttu-id="88641-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="88641-107">EXAMPLES</span></span>

### <span data-ttu-id="88641-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="88641-108">Example 1</span></span>
```
PS C:\> $serverDNSAlias = New-AzureRmSqlServerDnsAlias -ResourceGroupName rg -ServerName serverName -DnsAliasName aliasName

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
```

<span data-ttu-id="88641-109">Эта команда создает псевдоним DNS для Azure SQL Server с именем aliasName, указывающим на сервер serverName.</span><span class="sxs-lookup"><span data-stu-id="88641-109">This command creates Azure SQL Server DNS Alias with the name aliasName that is pointing to server serverName</span></span>

## <span data-ttu-id="88641-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="88641-110">PARAMETERS</span></span>

### <span data-ttu-id="88641-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="88641-111">-AsJob</span></span>
<span data-ttu-id="88641-112">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="88641-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="88641-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88641-113">-DefaultProfile</span></span>
<span data-ttu-id="88641-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="88641-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88641-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="88641-115">-Name</span></span>
<span data-ttu-id="88641-116">Имя псевдонима DNS для Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="88641-116">The Azure Sql Server Dns Alias name.</span></span>

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

### <span data-ttu-id="88641-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88641-117">-ResourceGroupName</span></span>
<span data-ttu-id="88641-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="88641-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="88641-119">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="88641-119">-ServerName</span></span>
<span data-ttu-id="88641-120">Имя сервера Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="88641-120">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="88641-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="88641-121">-Confirm</span></span>
<span data-ttu-id="88641-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="88641-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88641-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88641-123">-WhatIf</span></span>
<span data-ttu-id="88641-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="88641-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="88641-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="88641-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88641-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88641-126">CommonParameters</span></span>
<span data-ttu-id="88641-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="88641-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88641-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88641-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88641-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="88641-129">INPUTS</span></span>

### <span data-ttu-id="88641-130">System. String</span><span class="sxs-lookup"><span data-stu-id="88641-130">System.String</span></span>

## <span data-ttu-id="88641-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="88641-131">OUTPUTS</span></span>

### <span data-ttu-id="88641-132">Microsoft. Azure. Commands. SQL. ServerDnsAlias. Model. AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="88641-132">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="88641-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="88641-133">NOTES</span></span>

## <span data-ttu-id="88641-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="88641-134">RELATED LINKS</span></span>
