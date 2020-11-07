---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/remove-azurermdatalakestorevirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreVirtualNetworkRule.md
ms.openlocfilehash: 196d0eba5119ab984f9ffc632a301d3e65157f63
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732956"
---
# <span data-ttu-id="7dc57-101">Remove-AzureRmDataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="7dc57-101">Remove-AzureRmDataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="7dc57-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7dc57-102">SYNOPSIS</span></span>
<span data-ttu-id="7dc57-103">Удаляет указанное правило виртуальной сети в указанном Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="7dc57-103">Removes the specified virtual network rule in the specified Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7dc57-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7dc57-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeStoreVirtualNetworkRule [-Account] <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7dc57-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7dc57-105">DESCRIPTION</span></span>
<span data-ttu-id="7dc57-106">Командлет **Remove-AzureRmDataLakeStoreVirtualNetworkRule** удаляет указанное правило виртуальной сети в указанном Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="7dc57-106">The **Remove-AzureRmDataLakeStoreVirtualNetworkRule** cmdlet removes the specified virtual network rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="7dc57-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7dc57-107">EXAMPLES</span></span>

### <span data-ttu-id="7dc57-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7dc57-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmDataLakeStoreVirtualNetworkRule -Account "dls" -Name "myVNET"
```

<span data-ttu-id="7dc57-109">Удаление правила для виртуальной сети "myVNET" из списков рассылки "" \ мои учетные записи "</span><span class="sxs-lookup"><span data-stu-id="7dc57-109">Removes virtual network rule "myVNET" from account "dls"</span></span>

## <span data-ttu-id="7dc57-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7dc57-110">PARAMETERS</span></span>

### <span data-ttu-id="7dc57-111">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="7dc57-111">-Account</span></span>
<span data-ttu-id="7dc57-112">Учетная запись Data Lake Store для обновления правила виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="7dc57-112">The Data Lake Store account to update the virtual network rule in</span></span>

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

### <span data-ttu-id="7dc57-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7dc57-113">-DefaultProfile</span></span>
<span data-ttu-id="7dc57-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7dc57-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7dc57-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7dc57-115">-Name</span></span>
<span data-ttu-id="7dc57-116">Имя правила виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="7dc57-116">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="7dc57-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7dc57-117">-PassThru</span></span>
<span data-ttu-id="7dc57-118">Указывает, что должен возвращаться логический ответ, указывающий результат операции удаления.</span><span class="sxs-lookup"><span data-stu-id="7dc57-118">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7dc57-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7dc57-119">-Confirm</span></span>
<span data-ttu-id="7dc57-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7dc57-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7dc57-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7dc57-121">-WhatIf</span></span>
<span data-ttu-id="7dc57-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7dc57-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7dc57-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7dc57-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7dc57-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7dc57-124">CommonParameters</span></span>
<span data-ttu-id="7dc57-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7dc57-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7dc57-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7dc57-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7dc57-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7dc57-127">INPUTS</span></span>

### <span data-ttu-id="7dc57-128">System. String</span><span class="sxs-lookup"><span data-stu-id="7dc57-128">System.String</span></span>

### <span data-ttu-id="7dc57-129">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="7dc57-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="7dc57-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7dc57-130">OUTPUTS</span></span>

### <span data-ttu-id="7dc57-131">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7dc57-131">System.Boolean</span></span>

## <span data-ttu-id="7dc57-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="7dc57-132">NOTES</span></span>

## <span data-ttu-id="7dc57-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7dc57-133">RELATED LINKS</span></span>
