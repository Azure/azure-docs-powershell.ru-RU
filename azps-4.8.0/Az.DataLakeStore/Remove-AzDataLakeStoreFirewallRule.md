---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 6C7A7E1A-87A2-4F0D-9091-413C111F47F0
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/remove-azdatalakestorefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreFirewallRule.md
ms.openlocfilehash: e583379f9541c056943081b804a84ecd7bee7bf5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236230"
---
# <span data-ttu-id="5912f-101">Remove-AzDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="5912f-101">Remove-AzDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="5912f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5912f-102">SYNOPSIS</span></span>
<span data-ttu-id="5912f-103">Удаляет указанное правило брандмауэра в указанном Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="5912f-103">Removes the specified firewall rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="5912f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5912f-104">SYNTAX</span></span>

```
Remove-AzDataLakeStoreFirewallRule [-Account] <String> [[-Name] <String>] [-PassThru]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5912f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5912f-105">DESCRIPTION</span></span>
<span data-ttu-id="5912f-106">Командлет **Remove-AzDataLakeStoreFirewallRule** удаляет указанное правило брандмауэра в указанном Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="5912f-106">The **Remove-AzDataLakeStoreFirewallRule** cmdlet removes the specified firewall rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="5912f-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5912f-107">EXAMPLES</span></span>

### <span data-ttu-id="5912f-108">Пример 1: Удаление правила брандмауэра из учетной записи</span><span class="sxs-lookup"><span data-stu-id="5912f-108">Example 1: Remove a firewall rule from an account</span></span>
```
PS C:\> Remove-AzDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyFirewallRule
```

<span data-ttu-id="5912f-109">Удаление правила брандмауэра "MyFirewallRule" из учетной записи "ContosoADL"</span><span class="sxs-lookup"><span data-stu-id="5912f-109">Removes firewall rule "MyFirewallRule" from account "ContosoADL"</span></span>

## <span data-ttu-id="5912f-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5912f-110">PARAMETERS</span></span>

### <span data-ttu-id="5912f-111">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="5912f-111">-Account</span></span>
<span data-ttu-id="5912f-112">Учетная запись Data Lake Store для обновления правила брандмауэра в</span><span class="sxs-lookup"><span data-stu-id="5912f-112">The Data Lake Store account to update the firewall rule in</span></span>

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

### <span data-ttu-id="5912f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5912f-113">-DefaultProfile</span></span>
<span data-ttu-id="5912f-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="5912f-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5912f-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5912f-115">-Name</span></span>
<span data-ttu-id="5912f-116">Имя удаляемого правила брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="5912f-116">The name of the firewall rule to delete.</span></span>

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

### <span data-ttu-id="5912f-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5912f-117">-PassThru</span></span>
<span data-ttu-id="5912f-118">Указывает, что должен возвращаться логический ответ, указывающий результат операции удаления.</span><span class="sxs-lookup"><span data-stu-id="5912f-118">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="5912f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5912f-119">-ResourceGroupName</span></span>
<span data-ttu-id="5912f-120">Указывает имя группы ресурсов, которая содержит учетную запись, из которой нужно удалить правило брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="5912f-120">Specifies the name of the resource group that contains the account to remove the firewall rule from.</span></span>

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

### <span data-ttu-id="5912f-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5912f-121">-Confirm</span></span>
<span data-ttu-id="5912f-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5912f-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5912f-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5912f-123">-WhatIf</span></span>
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

### <span data-ttu-id="5912f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5912f-124">CommonParameters</span></span>
<span data-ttu-id="5912f-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5912f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5912f-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5912f-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5912f-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5912f-127">INPUTS</span></span>

### <span data-ttu-id="5912f-128">System. String</span><span class="sxs-lookup"><span data-stu-id="5912f-128">System.String</span></span>

### <span data-ttu-id="5912f-129">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="5912f-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="5912f-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5912f-130">OUTPUTS</span></span>

### <span data-ttu-id="5912f-131">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5912f-131">System.Boolean</span></span>

## <span data-ttu-id="5912f-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="5912f-132">NOTES</span></span>

## <span data-ttu-id="5912f-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5912f-133">RELATED LINKS</span></span>