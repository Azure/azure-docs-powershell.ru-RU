---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserveradvancedthreatprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvancedThreatProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvancedThreatProtectionPolicy.md
ms.openlocfilehash: dce8018e97e01c10356e77d321d564690cc03f71
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93728956"
---
# <span data-ttu-id="39a5c-101">Get-AzSqlServerAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="39a5c-101">Get-AzSqlServerAdvancedThreatProtectionPolicy</span></span>

## <span data-ttu-id="39a5c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="39a5c-102">SYNOPSIS</span></span>
<span data-ttu-id="39a5c-103">Возвращает политику Advanced Threat Protection для сервера.</span><span class="sxs-lookup"><span data-stu-id="39a5c-103">Gets Advanced Threat Protection policy of a server.</span></span>

## <span data-ttu-id="39a5c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="39a5c-104">SYNTAX</span></span>

```
Get-AzSqlServerAdvancedThreatProtectionPolicy [-InputObject <AzureSqlServerModel>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="39a5c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="39a5c-105">DESCRIPTION</span></span>
<span data-ttu-id="39a5c-106">Командлет **Get-AzSqlServerAdvancedThreatProtectionPolicy** retrives расширенной политики защиты от угроз для сервера.</span><span class="sxs-lookup"><span data-stu-id="39a5c-106">The **Get-AzSqlServerAdvancedThreatProtectionPolicy** cmdlet retrives the Advanced Threat Protection policy of a server.</span></span>

## <span data-ttu-id="39a5c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="39a5c-107">EXAMPLES</span></span>

### <span data-ttu-id="39a5c-108">Пример 1-получает сервер Advanced Threat protection</span><span class="sxs-lookup"><span data-stu-id="39a5c-108">Example 1 - Gets server Advanced Threat Protection</span></span>
```powershell
PS C:\>  Get-AzSqlServerAdvancedThreatProtectionPolicy `
            -ResourceGroupName "ResourceGroup01" `
            -ServerName "Server01" 

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

### <span data-ttu-id="39a5c-109">Пример 2: получение Advanced Threat protection из серверного ресурса</span><span class="sxs-lookup"><span data-stu-id="39a5c-109">Example 2 - Gets server Advanced Threat Protection from server resource</span></span>
```powershell
PS C:\>  Get-AzSqlServer `
           -ResourceGroupName "ResourceGroup01" `
           -ServerName "Server01" `
           | Get-AzSqlServerAdvancedThreatProtectionPolicy

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

## <span data-ttu-id="39a5c-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="39a5c-110">PARAMETERS</span></span>

### <span data-ttu-id="39a5c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39a5c-111">-DefaultProfile</span></span>
<span data-ttu-id="39a5c-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="39a5c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39a5c-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="39a5c-113">-InputObject</span></span>
<span data-ttu-id="39a5c-114">Объект сервера для использования с расширенной операцией политики защиты от угроз</span><span class="sxs-lookup"><span data-stu-id="39a5c-114">The server object to use with Advanced Threat Protection policy operation</span></span>

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

### <span data-ttu-id="39a5c-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39a5c-115">-ResourceGroupName</span></span>
<span data-ttu-id="39a5c-116">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="39a5c-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="39a5c-117">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="39a5c-117">-ServerName</span></span>
<span data-ttu-id="39a5c-118">Имя сервера базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="39a5c-118">SQL Database server name.</span></span>

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

### <span data-ttu-id="39a5c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39a5c-119">CommonParameters</span></span>
<span data-ttu-id="39a5c-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="39a5c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39a5c-121">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="39a5c-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39a5c-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="39a5c-122">INPUTS</span></span>

### <span data-ttu-id="39a5c-123">Microsoft. Azure. Commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="39a5c-123">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="39a5c-124">System. String</span><span class="sxs-lookup"><span data-stu-id="39a5c-124">System.String</span></span>

## <span data-ttu-id="39a5c-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="39a5c-125">OUTPUTS</span></span>

### <span data-ttu-id="39a5c-126">Microsoft. Azure. Commands. SQL. AdvancedThreatProtection. Model. ServerAdvancedThreatProtectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="39a5c-126">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedThreatProtectionPolicyModel</span></span>

## <span data-ttu-id="39a5c-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="39a5c-127">NOTES</span></span>

## <span data-ttu-id="39a5c-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="39a5c-128">RELATED LINKS</span></span>
