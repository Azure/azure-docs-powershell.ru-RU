---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverdnsalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDnsAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDnsAlias.md
ms.openlocfilehash: 417bab5679da4607cc42468fc4620cf392323919
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235293"
---
# <span data-ttu-id="314e2-101">Get-AzSqlServerDnsAlias</span><span class="sxs-lookup"><span data-stu-id="314e2-101">Get-AzSqlServerDnsAlias</span></span>

## <span data-ttu-id="314e2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="314e2-102">SYNOPSIS</span></span>
<span data-ttu-id="314e2-103">Получает или перечисляет DNS-псевдоним Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="314e2-103">Gets or lists Azure SQL Server DNS Alias.</span></span>

## <span data-ttu-id="314e2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="314e2-104">SYNTAX</span></span>

```
Get-AzSqlServerDnsAlias [-Name <String>] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="314e2-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="314e2-105">DESCRIPTION</span></span>
<span data-ttu-id="314e2-106">Получите конкретный DNS-псевдоним для Azure SQL Server или список всех DNS-псевдонимов сервера.</span><span class="sxs-lookup"><span data-stu-id="314e2-106">Get the specific Azure SQL Server DNS Alias or lists all Server DNS Aliases for the server</span></span>

## <span data-ttu-id="314e2-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="314e2-107">EXAMPLES</span></span>

### <span data-ttu-id="314e2-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="314e2-108">Example 1</span></span>
```
PS C:\> $serverDNSAliases = Get-AzSqlServerDNSAlias -ServerName servername -ResourceGroupName rgname

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
rgname             servername   dnsaliasname2
```

<span data-ttu-id="314e2-109">Вывод списка всех DNS-псевдонимов сервера для определенного сервера</span><span class="sxs-lookup"><span data-stu-id="314e2-109">Lists all Server DNS Aliases for the specific server</span></span>

### <span data-ttu-id="314e2-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="314e2-110">Example 2</span></span>
```
PS C:\> $serverDNSAliases = Get-AzSqlServerDNSAlias -DnsAliasName dnsaliasname -ServerName servername -ResourceGroupName rgname

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
```

<span data-ttu-id="314e2-111">Получает псевдоним DNS сервера, указанный именем сервера и псевдонимом.</span><span class="sxs-lookup"><span data-stu-id="314e2-111">Gets Server DNS Alias specified by server and alias name</span></span>

### <span data-ttu-id="314e2-112">Пример 3</span><span class="sxs-lookup"><span data-stu-id="314e2-112">Example 3</span></span>
```
PS C:\> $serverDNSAliases = Get-AzSqlServerDNSAlias -ServerName servername -ResourceGroupName rgname -DnsAliasName "dnsaliasname*"

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
rgname             servername   dnsaliasname2
```

<span data-ttu-id="314e2-113">Список всех DNS-псевдонимов сервера для определенного сервера, которые начинаются с "dnsaliasname".</span><span class="sxs-lookup"><span data-stu-id="314e2-113">Lists all Server DNS Aliases for the specific server that start with "dnsaliasname".</span></span>

## <span data-ttu-id="314e2-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="314e2-114">PARAMETERS</span></span>

### <span data-ttu-id="314e2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="314e2-115">-DefaultProfile</span></span>
<span data-ttu-id="314e2-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="314e2-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="314e2-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="314e2-117">-Name</span></span>
<span data-ttu-id="314e2-118">Имя псевдонима DNS для Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="314e2-118">The Azure Sql Server DNS Alias name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DnsAliasName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="314e2-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="314e2-119">-ResourceGroupName</span></span>
<span data-ttu-id="314e2-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="314e2-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="314e2-121">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="314e2-121">-ServerName</span></span>
<span data-ttu-id="314e2-122">Имя сервера Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="314e2-122">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="314e2-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="314e2-123">-Confirm</span></span>
<span data-ttu-id="314e2-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="314e2-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="314e2-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="314e2-125">-WhatIf</span></span>
<span data-ttu-id="314e2-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="314e2-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="314e2-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="314e2-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="314e2-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="314e2-128">CommonParameters</span></span>
<span data-ttu-id="314e2-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="314e2-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="314e2-130">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="314e2-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="314e2-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="314e2-131">INPUTS</span></span>

### <span data-ttu-id="314e2-132">System. String</span><span class="sxs-lookup"><span data-stu-id="314e2-132">System.String</span></span>

## <span data-ttu-id="314e2-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="314e2-133">OUTPUTS</span></span>

### <span data-ttu-id="314e2-134">Microsoft. Azure. Commands. SQL. ServerDnsAlias. Model. AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="314e2-134">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="314e2-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="314e2-135">NOTES</span></span>

## <span data-ttu-id="314e2-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="314e2-136">RELATED LINKS</span></span>
