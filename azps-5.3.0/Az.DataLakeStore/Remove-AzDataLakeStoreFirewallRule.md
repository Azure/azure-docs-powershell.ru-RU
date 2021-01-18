---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 6C7A7E1A-87A2-4F0D-9091-413C111F47F0
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/remove-azdatalakestorefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreFirewallRule.md
ms.openlocfilehash: e583379f9541c056943081b804a84ecd7bee7bf5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98504568"
---
# <span data-ttu-id="5dea2-101">Remove-AzDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="5dea2-101">Remove-AzDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="5dea2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5dea2-102">SYNOPSIS</span></span>
<span data-ttu-id="5dea2-103">Удаляет указанное правило брандмауэра для указанного магазина Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="5dea2-103">Removes the specified firewall rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="5dea2-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5dea2-104">SYNTAX</span></span>

```
Remove-AzDataLakeStoreFirewallRule [-Account] <String> [[-Name] <String>] [-PassThru]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5dea2-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5dea2-105">DESCRIPTION</span></span>
<span data-ttu-id="5dea2-106">С **помощью cmdlet Remove-AzDataLakeStoreFirewallRule** вы можете удалить указанное правило брандмауэра для указанного магазина Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="5dea2-106">The **Remove-AzDataLakeStoreFirewallRule** cmdlet removes the specified firewall rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="5dea2-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5dea2-107">EXAMPLES</span></span>

### <span data-ttu-id="5dea2-108">Пример 1. Удаление правила брандмауэра из учетной записи</span><span class="sxs-lookup"><span data-stu-id="5dea2-108">Example 1: Remove a firewall rule from an account</span></span>
```
PS C:\> Remove-AzDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyFirewallRule
```

<span data-ttu-id="5dea2-109">Удаляет правило брандмауэра "MyFirewallRule" из учетной записи ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="5dea2-109">Removes firewall rule "MyFirewallRule" from account "ContosoADL"</span></span>

## <span data-ttu-id="5dea2-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5dea2-110">PARAMETERS</span></span>

### <span data-ttu-id="5dea2-111">-Account</span><span class="sxs-lookup"><span data-stu-id="5dea2-111">-Account</span></span>
<span data-ttu-id="5dea2-112">Учетная запись магазина данных Для обновления правила брандмауэра в</span><span class="sxs-lookup"><span data-stu-id="5dea2-112">The Data Lake Store account to update the firewall rule in</span></span>

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

### <span data-ttu-id="5dea2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5dea2-113">-DefaultProfile</span></span>
<span data-ttu-id="5dea2-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="5dea2-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5dea2-115">-Name</span><span class="sxs-lookup"><span data-stu-id="5dea2-115">-Name</span></span>
<span data-ttu-id="5dea2-116">Имя правила брандмауэра, которое нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="5dea2-116">The name of the firewall rule to delete.</span></span>

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

### <span data-ttu-id="5dea2-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5dea2-117">-PassThru</span></span>
<span data-ttu-id="5dea2-118">Указывает на то, что должен быть возвращен boolean response, указывающий на результат операции удаления.</span><span class="sxs-lookup"><span data-stu-id="5dea2-118">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5dea2-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5dea2-119">-ResourceGroupName</span></span>
<span data-ttu-id="5dea2-120">Имя группы ресурсов, содержаной учетную запись, для удаления правила брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="5dea2-120">Specifies the name of the resource group that contains the account to remove the firewall rule from.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5dea2-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5dea2-121">-Confirm</span></span>
<span data-ttu-id="5dea2-122">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5dea2-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5dea2-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5dea2-123">-WhatIf</span></span>
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

### <span data-ttu-id="5dea2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5dea2-124">CommonParameters</span></span>
<span data-ttu-id="5dea2-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5dea2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5dea2-126">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5dea2-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5dea2-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5dea2-127">INPUTS</span></span>

### <span data-ttu-id="5dea2-128">System.String</span><span class="sxs-lookup"><span data-stu-id="5dea2-128">System.String</span></span>

### <span data-ttu-id="5dea2-129">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="5dea2-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="5dea2-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5dea2-130">OUTPUTS</span></span>

### <span data-ttu-id="5dea2-131">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5dea2-131">System.Boolean</span></span>

## <span data-ttu-id="5dea2-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5dea2-132">NOTES</span></span>

## <span data-ttu-id="5dea2-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5dea2-133">RELATED LINKS</span></span>
