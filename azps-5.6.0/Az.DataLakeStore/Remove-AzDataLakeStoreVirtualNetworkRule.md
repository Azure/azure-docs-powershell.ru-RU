---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/remove-azdatalakestorevirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreVirtualNetworkRule.md
ms.openlocfilehash: b5b9f154cb494aad7c1ef0faec130b4c4c1cc3d9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101962312"
---
# <span data-ttu-id="6cbd4-101">Remove-AzDataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="6cbd4-101">Remove-AzDataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="6cbd4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6cbd4-102">SYNOPSIS</span></span>
<span data-ttu-id="6cbd4-103">Удаляет указанное правило виртуальной сети из указанного магазина Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="6cbd4-103">Removes the specified virtual network rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="6cbd4-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6cbd4-104">SYNTAX</span></span>

```
Remove-AzDataLakeStoreVirtualNetworkRule [-Account] <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6cbd4-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6cbd4-105">DESCRIPTION</span></span>
<span data-ttu-id="6cbd4-106">Командлет **Remove-AzDataLakeStoreVirtualNetworkRule** удаляет указанное правило виртуальной сети в указанном Хранилище для озера данных.</span><span class="sxs-lookup"><span data-stu-id="6cbd4-106">The **Remove-AzDataLakeStoreVirtualNetworkRule** cmdlet removes the specified virtual network rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="6cbd4-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6cbd4-107">EXAMPLES</span></span>

### <span data-ttu-id="6cbd4-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6cbd4-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataLakeStoreVirtualNetworkRule -Account "dls" -Name "myVNET"
```

<span data-ttu-id="6cbd4-109">Удаляет правило виртуальной сети "myVNET" из учетной записи "dls"</span><span class="sxs-lookup"><span data-stu-id="6cbd4-109">Removes virtual network rule "myVNET" from account "dls"</span></span>

## <span data-ttu-id="6cbd4-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6cbd4-110">PARAMETERS</span></span>

### <span data-ttu-id="6cbd4-111">-Account</span><span class="sxs-lookup"><span data-stu-id="6cbd4-111">-Account</span></span>
<span data-ttu-id="6cbd4-112">Учетная запись Магазина данных для обновления виртуального правила сети в</span><span class="sxs-lookup"><span data-stu-id="6cbd4-112">The Data Lake Store account to update the virtual network rule in</span></span>

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

### <span data-ttu-id="6cbd4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cbd4-113">-DefaultProfile</span></span>
<span data-ttu-id="6cbd4-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6cbd4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6cbd4-115">-Name</span><span class="sxs-lookup"><span data-stu-id="6cbd4-115">-Name</span></span>
<span data-ttu-id="6cbd4-116">Имя виртуального правила сети.</span><span class="sxs-lookup"><span data-stu-id="6cbd4-116">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="6cbd4-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6cbd4-117">-PassThru</span></span>
<span data-ttu-id="6cbd4-118">Указывает на то, что должен быть возвращен boolean response, указывающий на результат операции удаления.</span><span class="sxs-lookup"><span data-stu-id="6cbd4-118">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="6cbd4-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6cbd4-119">-Confirm</span></span>
<span data-ttu-id="6cbd4-120">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6cbd4-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6cbd4-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6cbd4-121">-WhatIf</span></span>
<span data-ttu-id="6cbd4-122">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6cbd4-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6cbd4-123">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="6cbd4-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6cbd4-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cbd4-124">CommonParameters</span></span>
<span data-ttu-id="6cbd4-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6cbd4-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cbd4-126">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6cbd4-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cbd4-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6cbd4-127">INPUTS</span></span>

### <span data-ttu-id="6cbd4-128">System.String</span><span class="sxs-lookup"><span data-stu-id="6cbd4-128">System.String</span></span>

## <span data-ttu-id="6cbd4-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6cbd4-129">OUTPUTS</span></span>

### <span data-ttu-id="6cbd4-130">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6cbd4-130">System.Boolean</span></span>

## <span data-ttu-id="6cbd4-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6cbd4-131">NOTES</span></span>

## <span data-ttu-id="6cbd4-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6cbd4-132">RELATED LINKS</span></span>
