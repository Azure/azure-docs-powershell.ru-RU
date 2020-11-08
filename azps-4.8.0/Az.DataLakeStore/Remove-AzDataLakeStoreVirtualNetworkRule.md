---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/remove-azdatalakestorevirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreVirtualNetworkRule.md
ms.openlocfilehash: 9e455b7160b731f20e5dad6230b2015f73ca5390
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94077845"
---
# <span data-ttu-id="d7a62-101">Remove-AzDataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="d7a62-101">Remove-AzDataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="d7a62-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d7a62-102">SYNOPSIS</span></span>
<span data-ttu-id="d7a62-103">Удаляет указанное правило виртуальной сети в указанном Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="d7a62-103">Removes the specified virtual network rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="d7a62-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d7a62-104">SYNTAX</span></span>

```
Remove-AzDataLakeStoreVirtualNetworkRule [-Account] <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d7a62-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d7a62-105">DESCRIPTION</span></span>
<span data-ttu-id="d7a62-106">Командлет **Remove-AzDataLakeStoreVirtualNetworkRule** удаляет указанное правило виртуальной сети в указанном Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="d7a62-106">The **Remove-AzDataLakeStoreVirtualNetworkRule** cmdlet removes the specified virtual network rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="d7a62-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d7a62-107">EXAMPLES</span></span>

### <span data-ttu-id="d7a62-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d7a62-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataLakeStoreVirtualNetworkRule -Account "dls" -Name "myVNET"
```

<span data-ttu-id="d7a62-109">Удаление правила для виртуальной сети "myVNET" из списков рассылки "" \ мои учетные записи "</span><span class="sxs-lookup"><span data-stu-id="d7a62-109">Removes virtual network rule "myVNET" from account "dls"</span></span>

## <span data-ttu-id="d7a62-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d7a62-110">PARAMETERS</span></span>

### <span data-ttu-id="d7a62-111">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="d7a62-111">-Account</span></span>
<span data-ttu-id="d7a62-112">Учетная запись Data Lake Store для обновления правила виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="d7a62-112">The Data Lake Store account to update the virtual network rule in</span></span>

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

### <span data-ttu-id="d7a62-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7a62-113">-DefaultProfile</span></span>
<span data-ttu-id="d7a62-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d7a62-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d7a62-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d7a62-115">-Name</span></span>
<span data-ttu-id="d7a62-116">Имя правила виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="d7a62-116">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="d7a62-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d7a62-117">-PassThru</span></span>
<span data-ttu-id="d7a62-118">Указывает, что должен возвращаться логический ответ, указывающий результат операции удаления.</span><span class="sxs-lookup"><span data-stu-id="d7a62-118">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="d7a62-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d7a62-119">-Confirm</span></span>
<span data-ttu-id="d7a62-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d7a62-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7a62-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7a62-121">-WhatIf</span></span>
<span data-ttu-id="d7a62-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d7a62-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7a62-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d7a62-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7a62-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7a62-124">CommonParameters</span></span>
<span data-ttu-id="d7a62-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d7a62-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7a62-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7a62-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7a62-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d7a62-127">INPUTS</span></span>

### <span data-ttu-id="d7a62-128">System. String</span><span class="sxs-lookup"><span data-stu-id="d7a62-128">System.String</span></span>

## <span data-ttu-id="d7a62-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d7a62-129">OUTPUTS</span></span>

### <span data-ttu-id="d7a62-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d7a62-130">System.Boolean</span></span>

## <span data-ttu-id="d7a62-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="d7a62-131">NOTES</span></span>

## <span data-ttu-id="d7a62-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d7a62-132">RELATED LINKS</span></span>
