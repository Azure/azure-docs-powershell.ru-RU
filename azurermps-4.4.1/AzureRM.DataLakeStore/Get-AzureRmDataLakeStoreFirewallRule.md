---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 7D27F7B1-BAF8-4A01-8BA7-A75A4CFAE370
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreFirewallRule.md
ms.openlocfilehash: 8c7d936f8ea64534016286e97b34d36f41a72cf7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733756"
---
# <span data-ttu-id="cb81c-101">Get-AzureRmDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="cb81c-101">Get-AzureRmDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="cb81c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cb81c-102">SYNOPSIS</span></span>
<span data-ttu-id="cb81c-103">Получает указанные правила брандмауэра в заданном Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="cb81c-103">Gets the specified firewall rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="cb81c-104">Если не указано правило брандмауэра, выводится список всех правил брандмауэра для учетной записи.</span><span class="sxs-lookup"><span data-stu-id="cb81c-104">If no firewall rule is specified, then lists all firewall rules for the account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cb81c-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cb81c-105">SYNTAX</span></span>

```
Get-AzureRmDataLakeStoreFirewallRule [-Account] <String> [[-Name] <String>] [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cb81c-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cb81c-106">DESCRIPTION</span></span>
<span data-ttu-id="cb81c-107">Командлет Get-AzureRmDataLakeStoreFirewallRule получает указанные правила брандмауэра в указанном Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="cb81c-107">The Get-AzureRmDataLakeStoreFirewallRule cmdlet gets the specified firewall rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="cb81c-108">Если не указано правило брандмауэра, выводится список всех правил брандмауэра для учетной записи.</span><span class="sxs-lookup"><span data-stu-id="cb81c-108">If no firewall rule is specified, then lists all firewall rules for the account.</span></span>

## <span data-ttu-id="cb81c-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cb81c-109">EXAMPLES</span></span>

### <span data-ttu-id="cb81c-110">Пример 1: получение определенного правила брандмауэра</span><span class="sxs-lookup"><span data-stu-id="cb81c-110">Example 1: Retrieve a specific firewall rule</span></span>
```
PS C:\> Get-AzureRmDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyFirewallRule
```

<span data-ttu-id="cb81c-111">Возвращает правило брандмауэра с именем "MyFirewallRule" из учетной записи "ContosoADL"</span><span class="sxs-lookup"><span data-stu-id="cb81c-111">Returns the firewall rule named "MyFirewallRule" from account "ContosoADL"</span></span>

### <span data-ttu-id="cb81c-112">Пример 2: список всех правил брандмауэра в учетной записи</span><span class="sxs-lookup"><span data-stu-id="cb81c-112">Example 2: List all firewall rules in an account</span></span>
```
PS C:\> Get-AzureRmDataLakeStoreFirewallRule -AccountName "ContosoADL"
```

<span data-ttu-id="cb81c-113">Возвращает все правила брандмауэра в учетной записи "ContosoADL".</span><span class="sxs-lookup"><span data-stu-id="cb81c-113">Returns all firewall rules in account "ContosoADL"</span></span>

## <span data-ttu-id="cb81c-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cb81c-114">PARAMETERS</span></span>

### <span data-ttu-id="cb81c-115">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="cb81c-115">-Account</span></span>
<span data-ttu-id="cb81c-116">Учетная запись Data Lake Store, из которой нужно получить правило брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="cb81c-116">The Data Lake Store account to retrieve the firewall rule from.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb81c-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="cb81c-117">-Name</span></span>
<span data-ttu-id="cb81c-118">Имя правила межсетевого экрана, которое требуется получить</span><span class="sxs-lookup"><span data-stu-id="cb81c-118">The name of the firewall rule to retrieve</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb81c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb81c-119">-ResourceGroupName</span></span>
<span data-ttu-id="cb81c-120">Имя группы ресурсов, для которой требуется извлечь указанное правило брандмауэра для указанной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="cb81c-120">Name of resource group under which want to retrieve the specified account's specified firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb81c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb81c-121">-DefaultProfile</span></span>
<span data-ttu-id="cb81c-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cb81c-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cb81c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb81c-123">CommonParameters</span></span>
<span data-ttu-id="cb81c-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cb81c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb81c-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb81c-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb81c-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cb81c-126">INPUTS</span></span>

## <span data-ttu-id="cb81c-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cb81c-127">OUTPUTS</span></span>

### <span data-ttu-id="cb81c-128">DataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="cb81c-128">DataLakeStoreFirewallRule</span></span>
<span data-ttu-id="cb81c-129">Указанное правило брандмауэра, которое требуется получить</span><span class="sxs-lookup"><span data-stu-id="cb81c-129">The specified firewall rule to retrieve</span></span>

### <span data-ttu-id="cb81c-130">Оставлял<DataLakeStoreFirewallRule></span><span class="sxs-lookup"><span data-stu-id="cb81c-130">IList<DataLakeStoreFirewallRule></span></span>
<span data-ttu-id="cb81c-131">Список правил брандмауэра в указанной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="cb81c-131">The list of firewall rules in the specified account.</span></span>

## <span data-ttu-id="cb81c-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="cb81c-132">NOTES</span></span>

## <span data-ttu-id="cb81c-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cb81c-133">RELATED LINKS</span></span>

