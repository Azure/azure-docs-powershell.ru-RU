---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/disable-azsqlserveradvancedthreatprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlServerAdvancedThreatProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlServerAdvancedThreatProtection.md
ms.openlocfilehash: d6a06c3f4c50e10522ed06e6b1cd4185c1ef6768
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93729059"
---
# <span data-ttu-id="5ab73-101">Disable-AzSqlServerAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="5ab73-101">Disable-AzSqlServerAdvancedThreatProtection</span></span>

## <span data-ttu-id="5ab73-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5ab73-102">SYNOPSIS</span></span>
<span data-ttu-id="5ab73-103">Отключение Advanced Threat Protection на сервере.</span><span class="sxs-lookup"><span data-stu-id="5ab73-103">Disables Advanced Threat Protection on a server.</span></span>

## <span data-ttu-id="5ab73-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5ab73-104">SYNTAX</span></span>

```
Disable-AzSqlServerAdvancedThreatProtection [-InputObject <AzureSqlServerModel>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5ab73-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5ab73-105">DESCRIPTION</span></span>
<span data-ttu-id="5ab73-106">Командлет **Disable-AzSqlServerAdvancedThreatProtection** отключает Advanced Threat Protection на сервере.</span><span class="sxs-lookup"><span data-stu-id="5ab73-106">The **Disable-AzSqlServerAdvancedThreatProtection** cmdlet disables Advanced Threat Protection on a server.</span></span>

## <span data-ttu-id="5ab73-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5ab73-107">EXAMPLES</span></span>

### <span data-ttu-id="5ab73-108">Пример 1: отключение Advanced Threat Protection на сервере</span><span class="sxs-lookup"><span data-stu-id="5ab73-108">Example 1 - Disable server Advanced Threat Protection</span></span>
```powershell
PS C:\>  Disable-AzSqlServerAdvancedThreatProtection `
            -ResourceGroupName "ResourceGroup01" `
            -ServerName "Server01" 

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : False
```

### <span data-ttu-id="5ab73-109">Пример 2: отключение Advanced Threat Protection для серверного ресурса</span><span class="sxs-lookup"><span data-stu-id="5ab73-109">Example 2 - Disable server Advanced Threat Protection from server resource</span></span>
```powershell
PS C:\>  Get-AzSqlServer `
           -ResourceGroupName "ResourceGroup01" `
           -ServerName "Server01" `
           | Disable-AzSqlServerAdvancedThreatProtection

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : False
```

## <span data-ttu-id="5ab73-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5ab73-110">PARAMETERS</span></span>

### <span data-ttu-id="5ab73-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ab73-111">-DefaultProfile</span></span>
<span data-ttu-id="5ab73-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5ab73-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5ab73-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5ab73-113">-InputObject</span></span>
<span data-ttu-id="5ab73-114">Объект сервера для использования с расширенной операцией политики защиты от угроз</span><span class="sxs-lookup"><span data-stu-id="5ab73-114">The server object to use with Advanced Threat Protection policy operation</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5ab73-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ab73-115">-ResourceGroupName</span></span>
<span data-ttu-id="5ab73-116">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5ab73-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="5ab73-117">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="5ab73-117">-ServerName</span></span>
<span data-ttu-id="5ab73-118">Имя сервера базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="5ab73-118">SQL Database server name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ab73-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5ab73-119">-Confirm</span></span>
<span data-ttu-id="5ab73-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5ab73-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ab73-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ab73-121">-WhatIf</span></span>
<span data-ttu-id="5ab73-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5ab73-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5ab73-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5ab73-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ab73-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ab73-124">CommonParameters</span></span>
<span data-ttu-id="5ab73-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5ab73-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ab73-126">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5ab73-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ab73-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5ab73-127">INPUTS</span></span>

### <span data-ttu-id="5ab73-128">Microsoft. Azure. Commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="5ab73-128">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="5ab73-129">System. String</span><span class="sxs-lookup"><span data-stu-id="5ab73-129">System.String</span></span>

## <span data-ttu-id="5ab73-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5ab73-130">OUTPUTS</span></span>

### <span data-ttu-id="5ab73-131">Microsoft. Azure. Commands. SQL. AdvancedThreatProtection. Model. ServerAdvancedThreatProtectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="5ab73-131">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedThreatProtectionPolicyModel</span></span>

## <span data-ttu-id="5ab73-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="5ab73-132">NOTES</span></span>

## <span data-ttu-id="5ab73-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5ab73-133">RELATED LINKS</span></span>
