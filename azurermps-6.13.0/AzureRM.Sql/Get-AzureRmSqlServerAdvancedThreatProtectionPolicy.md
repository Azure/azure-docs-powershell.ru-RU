---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserveradvancedthreatprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerAdvancedThreatProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerAdvancedThreatProtectionPolicy.md
ms.openlocfilehash: 16762b56995b90422c78ad6dc5dd87461c0a8317
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566383"
---
# <span data-ttu-id="2a4f7-101">Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="2a4f7-101">Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span></span>

## <span data-ttu-id="2a4f7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2a4f7-102">SYNOPSIS</span></span>
<span data-ttu-id="2a4f7-103">Возвращает политику Advanced Threat Protection для сервера.</span><span class="sxs-lookup"><span data-stu-id="2a4f7-103">Gets Advanced Threat Protection policy of a server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2a4f7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2a4f7-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerAdvancedThreatProtectionPolicy [-InputObject <AzureSqlServerModel>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2a4f7-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2a4f7-105">DESCRIPTION</span></span>
<span data-ttu-id="2a4f7-106">Командлет **Get-AzureRmSqlServerAdvancedThreatProtectionPolicy** retrives расширенной политики защиты от угроз для сервера.</span><span class="sxs-lookup"><span data-stu-id="2a4f7-106">The **Get-AzureRmSqlServerAdvancedThreatProtectionPolicy** cmdlet retrives the Advanced Threat Protection policy of a server.</span></span>

## <span data-ttu-id="2a4f7-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2a4f7-107">EXAMPLES</span></span>

### <span data-ttu-id="2a4f7-108">Пример 1-получает сервер Advanced Threat protection</span><span class="sxs-lookup"><span data-stu-id="2a4f7-108">Example 1 - Gets server Advanced Threat Protection</span></span>
```powershell
PS C:\>  Get-AzureRmSqlServerAdvancedThreatProtectionPolicy `
            -ResourceGroupName "ResourceGroup01" `
            -ServerName "Server01" 

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

### <span data-ttu-id="2a4f7-109">Пример 2: получение Advanced Threat protection из серверного ресурса</span><span class="sxs-lookup"><span data-stu-id="2a4f7-109">Example 2 - Gets server Advanced Threat Protection from server resource</span></span>
```powershell
PS C:\>  Get-AzureRmSqlServer `
           -ResourceGroupName "ResourceGroup01" `
           -ServerName "Server01" `
           | Get-AzureRmSqlServerAdvancedThreatProtectionPolicy

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

## <span data-ttu-id="2a4f7-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2a4f7-110">PARAMETERS</span></span>

### <span data-ttu-id="2a4f7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a4f7-111">-DefaultProfile</span></span>
<span data-ttu-id="2a4f7-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2a4f7-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2a4f7-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2a4f7-113">-InputObject</span></span>
<span data-ttu-id="2a4f7-114">Объект сервера для использования с расширенной операцией политики защиты от угроз</span><span class="sxs-lookup"><span data-stu-id="2a4f7-114">The server object to use with Advanced Threat Protection policy operation</span></span>

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

### <span data-ttu-id="2a4f7-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a4f7-115">-ResourceGroupName</span></span>
<span data-ttu-id="2a4f7-116">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2a4f7-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="2a4f7-117">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="2a4f7-117">-ServerName</span></span>
<span data-ttu-id="2a4f7-118">Имя сервера базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="2a4f7-118">SQL Database server name.</span></span>

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

### <span data-ttu-id="2a4f7-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a4f7-119">CommonParameters</span></span>
<span data-ttu-id="2a4f7-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2a4f7-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a4f7-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a4f7-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a4f7-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2a4f7-122">INPUTS</span></span>

### <span data-ttu-id="2a4f7-123">Microsoft. Azure. Commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="2a4f7-123">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>
<span data-ttu-id="2a4f7-124">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="2a4f7-124">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="2a4f7-125">System. String</span><span class="sxs-lookup"><span data-stu-id="2a4f7-125">System.String</span></span>

## <span data-ttu-id="2a4f7-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2a4f7-126">OUTPUTS</span></span>

### <span data-ttu-id="2a4f7-127">Microsoft. Azure. Commands. SQL. AdvancedThreatProtection. Model. ServerAdvancedThreatProtectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="2a4f7-127">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedThreatProtectionPolicyModel</span></span>

## <span data-ttu-id="2a4f7-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="2a4f7-128">NOTES</span></span>

## <span data-ttu-id="2a4f7-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2a4f7-129">RELATED LINKS</span></span>
