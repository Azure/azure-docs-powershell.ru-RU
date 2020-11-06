---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/disable-azurermsqlserveradvancedthreatprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Disable-AzureRmSqlServerAdvancedThreatProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Disable-AzureRmSqlServerAdvancedThreatProtection.md
ms.openlocfilehash: cc38d619b810f2567594c0c1020190c271dc9f33
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562584"
---
# <span data-ttu-id="d8d99-101">Disable-AzureRmSqlServerAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="d8d99-101">Disable-AzureRmSqlServerAdvancedThreatProtection</span></span>

## <span data-ttu-id="d8d99-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d8d99-102">SYNOPSIS</span></span>
<span data-ttu-id="d8d99-103">Отключение Advanced Threat Protection на сервере.</span><span class="sxs-lookup"><span data-stu-id="d8d99-103">Disables Advanced Threat Protection on a server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d8d99-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d8d99-104">SYNTAX</span></span>

```
Disable-AzureRmSqlServerAdvancedThreatProtection [-InputObject <AzureSqlServerModel>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d8d99-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d8d99-105">DESCRIPTION</span></span>
<span data-ttu-id="d8d99-106">Командлет **Disable-AzureRmSqlServerAdvancedThreatProtection** отключает Advanced Threat Protection на сервере.</span><span class="sxs-lookup"><span data-stu-id="d8d99-106">The **Disable-AzureRmSqlServerAdvancedThreatProtection** cmdlet disables Advanced Threat Protection on a server.</span></span>

## <span data-ttu-id="d8d99-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d8d99-107">EXAMPLES</span></span>

### <span data-ttu-id="d8d99-108">Пример 1: отключение Advanced Threat Protection на сервере</span><span class="sxs-lookup"><span data-stu-id="d8d99-108">Example 1 - Disable server Advanced Threat Protection</span></span>
```powershell
PS C:\>  Disable-AzureRmSqlServerAdvancedThreatProtection `
            -ResourceGroupName "ResourceGroup01" `
            -ServerName "Server01" 

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : False
```

### <span data-ttu-id="d8d99-109">Пример 2: отключение Advanced Threat Protection для серверного ресурса</span><span class="sxs-lookup"><span data-stu-id="d8d99-109">Example 2 - Disable server Advanced Threat Protection from server resource</span></span>
```powershell
PS C:\>  Get-AzureRmSqlServer `
           -ResourceGroupName "ResourceGroup01" `
           -ServerName "Server01" `
           | Disable-AzureRmSqlServerAdvancedThreatProtection

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : False
```

## <span data-ttu-id="d8d99-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d8d99-110">PARAMETERS</span></span>

### <span data-ttu-id="d8d99-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8d99-111">-DefaultProfile</span></span>
<span data-ttu-id="d8d99-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d8d99-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d8d99-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d8d99-113">-InputObject</span></span>
<span data-ttu-id="d8d99-114">Объект сервера для использования с расширенной операцией политики защиты от угроз</span><span class="sxs-lookup"><span data-stu-id="d8d99-114">The server object to use with Advanced Threat Protection policy operation</span></span>

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

### <span data-ttu-id="d8d99-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8d99-115">-ResourceGroupName</span></span>
<span data-ttu-id="d8d99-116">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d8d99-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="d8d99-117">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="d8d99-117">-ServerName</span></span>
<span data-ttu-id="d8d99-118">Имя сервера базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="d8d99-118">SQL Database server name.</span></span>

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

### <span data-ttu-id="d8d99-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d8d99-119">-Confirm</span></span>
<span data-ttu-id="d8d99-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d8d99-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8d99-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8d99-121">-WhatIf</span></span>
<span data-ttu-id="d8d99-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d8d99-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d8d99-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d8d99-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8d99-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8d99-124">CommonParameters</span></span>
<span data-ttu-id="d8d99-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d8d99-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8d99-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8d99-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8d99-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d8d99-127">INPUTS</span></span>

### <span data-ttu-id="d8d99-128">Microsoft. Azure. Commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="d8d99-128">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>
<span data-ttu-id="d8d99-129">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d8d99-129">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="d8d99-130">System. String</span><span class="sxs-lookup"><span data-stu-id="d8d99-130">System.String</span></span>

## <span data-ttu-id="d8d99-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d8d99-131">OUTPUTS</span></span>

### <span data-ttu-id="d8d99-132">Microsoft. Azure. Commands. SQL. AdvancedThreatProtection. Model. ServerAdvancedThreatProtectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="d8d99-132">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedThreatProtectionPolicyModel</span></span>

## <span data-ttu-id="d8d99-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="d8d99-133">NOTES</span></span>

## <span data-ttu-id="d8d99-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d8d99-134">RELATED LINKS</span></span>
