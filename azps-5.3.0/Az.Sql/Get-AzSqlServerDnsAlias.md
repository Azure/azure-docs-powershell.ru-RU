---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverdnsalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDnsAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDnsAlias.md
ms.openlocfilehash: 417bab5679da4607cc42468fc4620cf392323919
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98508022"
---
# <span data-ttu-id="5e804-101">Get-AzSqlServerDnsAlias</span><span class="sxs-lookup"><span data-stu-id="5e804-101">Get-AzSqlServerDnsAlias</span></span>

## <span data-ttu-id="5e804-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5e804-102">SYNOPSIS</span></span>
<span data-ttu-id="5e804-103">Получает или перечисляет псевдоним DNS Azure SQL Server Azure.</span><span class="sxs-lookup"><span data-stu-id="5e804-103">Gets or lists Azure SQL Server DNS Alias.</span></span>

## <span data-ttu-id="5e804-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5e804-104">SYNTAX</span></span>

```
Get-AzSqlServerDnsAlias [-Name <String>] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e804-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5e804-105">DESCRIPTION</span></span>
<span data-ttu-id="5e804-106">Получите определенный псевдоним DNS для Azure SQL Server или укаймьте все псевдонимы DNS-сервера для сервера</span><span class="sxs-lookup"><span data-stu-id="5e804-106">Get the specific Azure SQL Server DNS Alias or lists all Server DNS Aliases for the server</span></span>

## <span data-ttu-id="5e804-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5e804-107">EXAMPLES</span></span>

### <span data-ttu-id="5e804-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5e804-108">Example 1</span></span>
```
PS C:\> $serverDNSAliases = Get-AzSqlServerDNSAlias -ServerName servername -ResourceGroupName rgname

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
rgname             servername   dnsaliasname2
```

<span data-ttu-id="5e804-109">Список всех псевдонимов DNS сервера для определенного сервера</span><span class="sxs-lookup"><span data-stu-id="5e804-109">Lists all Server DNS Aliases for the specific server</span></span>

### <span data-ttu-id="5e804-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="5e804-110">Example 2</span></span>
```
PS C:\> $serverDNSAliases = Get-AzSqlServerDNSAlias -DnsAliasName dnsaliasname -ServerName servername -ResourceGroupName rgname

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
```

<span data-ttu-id="5e804-111">Gets Server DNS Alias specified by server and alias name</span><span class="sxs-lookup"><span data-stu-id="5e804-111">Gets Server DNS Alias specified by server and alias name</span></span>

### <span data-ttu-id="5e804-112">Пример 3</span><span class="sxs-lookup"><span data-stu-id="5e804-112">Example 3</span></span>
```
PS C:\> $serverDNSAliases = Get-AzSqlServerDNSAlias -ServerName servername -ResourceGroupName rgname -DnsAliasName "dnsaliasname*"

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
rgname             servername   dnsaliasname2
```

<span data-ttu-id="5e804-113">Список всех псевдонимов DNS сервера для определенного сервера, который начинается с "dnsaliasname".</span><span class="sxs-lookup"><span data-stu-id="5e804-113">Lists all Server DNS Aliases for the specific server that start with "dnsaliasname".</span></span>

## <span data-ttu-id="5e804-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5e804-114">PARAMETERS</span></span>

### <span data-ttu-id="5e804-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e804-115">-DefaultProfile</span></span>
<span data-ttu-id="5e804-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5e804-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5e804-117">-Name</span><span class="sxs-lookup"><span data-stu-id="5e804-117">-Name</span></span>
<span data-ttu-id="5e804-118">Имя псевдонима DNS для Azure Sql Server.</span><span class="sxs-lookup"><span data-stu-id="5e804-118">The Azure Sql Server DNS Alias name.</span></span>

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

### <span data-ttu-id="5e804-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e804-119">-ResourceGroupName</span></span>
<span data-ttu-id="5e804-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5e804-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="5e804-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="5e804-121">-ServerName</span></span>
<span data-ttu-id="5e804-122">Имя Azure Sql Server.</span><span class="sxs-lookup"><span data-stu-id="5e804-122">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="5e804-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5e804-123">-Confirm</span></span>
<span data-ttu-id="5e804-124">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="5e804-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e804-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e804-125">-WhatIf</span></span>
<span data-ttu-id="5e804-126">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5e804-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e804-127">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="5e804-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e804-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e804-128">CommonParameters</span></span>
<span data-ttu-id="5e804-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e804-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e804-130">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5e804-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e804-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5e804-131">INPUTS</span></span>

### <span data-ttu-id="5e804-132">System.String</span><span class="sxs-lookup"><span data-stu-id="5e804-132">System.String</span></span>

## <span data-ttu-id="5e804-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5e804-133">OUTPUTS</span></span>

### <span data-ttu-id="5e804-134">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="5e804-134">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="5e804-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5e804-135">NOTES</span></span>

## <span data-ttu-id="5e804-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5e804-136">RELATED LINKS</span></span>
