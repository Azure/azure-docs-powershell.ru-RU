---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/enable-azsqlserveradvancedthreatprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlServerAdvancedThreatProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlServerAdvancedThreatProtection.md
ms.openlocfilehash: aaaf417137bb1ec16150a2bf3d0ac88b64e70fae
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93729057"
---
# <span data-ttu-id="c2682-101">Enable-AzSqlServerAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="c2682-101">Enable-AzSqlServerAdvancedThreatProtection</span></span>

## <span data-ttu-id="c2682-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c2682-102">SYNOPSIS</span></span>
<span data-ttu-id="c2682-103">Включает Advanced Threat Protection на сервере.</span><span class="sxs-lookup"><span data-stu-id="c2682-103">Enables Advanced Threat Protection on a server.</span></span>

## <span data-ttu-id="c2682-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c2682-104">SYNTAX</span></span>

```
Enable-AzSqlServerAdvancedThreatProtection [-InputObject <AzureSqlServerModel>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c2682-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c2682-105">DESCRIPTION</span></span>
<span data-ttu-id="c2682-106">Командлет **Enable-AzSqlServerAdvancedThreatProtection** включает Advanced Threat Protection на сервере.</span><span class="sxs-lookup"><span data-stu-id="c2682-106">The **Enable-AzSqlServerAdvancedThreatProtection** cmdlet enables Advanced Threat Protection on a server.</span></span>

## <span data-ttu-id="c2682-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c2682-107">EXAMPLES</span></span>

### <span data-ttu-id="c2682-108">Пример 1: Включение расширенной защиты от угроз для сервера</span><span class="sxs-lookup"><span data-stu-id="c2682-108">Example 1 - Enable server Advanced Threat Protection</span></span>
```powershell
PS C:\>  Enable-AzSqlServerAdvancedThreatProtection `
            -ResourceGroupName "ResourceGroup01" `
            -ServerName "Server01" 

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

### <span data-ttu-id="c2682-109">Пример 2: Включение Advanced Threat protection из серверного ресурса</span><span class="sxs-lookup"><span data-stu-id="c2682-109">Example 2 - Enable server Advanced Threat Protection from server resource</span></span>
```powershell
PS C:\>  Get-AzSqlServer `
           -ResourceGroupName "ResourceGroup01" `
           -ServerName "Server01" `
           | Enable-AzSqlServerAdvancedThreatProtection

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

## <span data-ttu-id="c2682-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c2682-110">PARAMETERS</span></span>

### <span data-ttu-id="c2682-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2682-111">-DefaultProfile</span></span>
<span data-ttu-id="c2682-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c2682-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2682-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c2682-113">-InputObject</span></span>
<span data-ttu-id="c2682-114">Объект сервера для использования с расширенной операцией политики защиты от угроз</span><span class="sxs-lookup"><span data-stu-id="c2682-114">The server object to use with Advanced Threat Protection policy operation</span></span>

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

### <span data-ttu-id="c2682-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2682-115">-ResourceGroupName</span></span>
<span data-ttu-id="c2682-116">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c2682-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="c2682-117">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="c2682-117">-ServerName</span></span>
<span data-ttu-id="c2682-118">Имя сервера базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="c2682-118">SQL Database server name.</span></span>

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

### <span data-ttu-id="c2682-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c2682-119">-Confirm</span></span>
<span data-ttu-id="c2682-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c2682-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2682-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2682-121">-WhatIf</span></span>
<span data-ttu-id="c2682-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c2682-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c2682-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c2682-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2682-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2682-124">CommonParameters</span></span>
<span data-ttu-id="c2682-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c2682-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2682-126">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c2682-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2682-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c2682-127">INPUTS</span></span>

### <span data-ttu-id="c2682-128">Microsoft. Azure. Commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="c2682-128">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="c2682-129">System. String</span><span class="sxs-lookup"><span data-stu-id="c2682-129">System.String</span></span>

## <span data-ttu-id="c2682-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c2682-130">OUTPUTS</span></span>

### <span data-ttu-id="c2682-131">Microsoft. Azure. Commands. SQL. AdvancedThreatProtection. Model. ServerAdvancedThreatProtectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="c2682-131">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedThreatProtectionPolicyModel</span></span>

## <span data-ttu-id="c2682-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="c2682-132">NOTES</span></span>

## <span data-ttu-id="c2682-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c2682-133">RELATED LINKS</span></span>
