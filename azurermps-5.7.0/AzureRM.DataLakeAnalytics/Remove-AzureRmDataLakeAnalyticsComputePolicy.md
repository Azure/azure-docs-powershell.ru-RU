---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/remove-azurermdatalakeanalyticscomputepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 5604430c795f7a318e18b89928c3a75d063a316a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563604"
---
# <span data-ttu-id="c5e7a-101">Remove-AzureRmDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="c5e7a-101">Remove-AzureRmDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="c5e7a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c5e7a-102">SYNOPSIS</span></span>
<span data-ttu-id="c5e7a-103">Удаляет указанную политику вычисления данных Azure Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="c5e7a-103">Removes a specified Azure Data Lake Analytics compute policy</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c5e7a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c5e7a-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [-Name] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c5e7a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c5e7a-105">DESCRIPTION</span></span>
<span data-ttu-id="c5e7a-106">Параметр **Remove-AzureRmDataLakeAnalyticsComputePolicy** удаляет указанную политику вычисления Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="c5e7a-106">The **Remove-AzureRmDataLakeAnalyticsComputePolicy** removes a specified Azure Data Lake Analytics compute policy.</span></span>

## <span data-ttu-id="c5e7a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c5e7a-107">EXAMPLES</span></span>

### <span data-ttu-id="c5e7a-108">Пример 1: Удаление политики вычислений</span><span class="sxs-lookup"><span data-stu-id="c5e7a-108">Example 1: Remove a compute policy</span></span>
```
PS C:\>Remove-AzureRmDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name myPolicy
```

<span data-ttu-id="c5e7a-109">Эта команда удаляет указанную политику вычислений с именем "myPolicy" в учетной записи "contosoadla".</span><span class="sxs-lookup"><span data-stu-id="c5e7a-109">This command removes the specified compute policy with name 'myPolicy' in account 'contosoadla'.</span></span>

## <span data-ttu-id="c5e7a-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c5e7a-110">PARAMETERS</span></span>

### <span data-ttu-id="c5e7a-111">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="c5e7a-111">-Account</span></span>
<span data-ttu-id="c5e7a-112">Имя учетной записи, из которой нужно удалить политику вычислений.</span><span class="sxs-lookup"><span data-stu-id="c5e7a-112">Name of the account to remove the compute policy from.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5e7a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5e7a-113">-DefaultProfile</span></span>
<span data-ttu-id="c5e7a-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="c5e7a-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5e7a-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c5e7a-115">-Name</span></span>
<span data-ttu-id="c5e7a-116">Имя удаляемой политики вычисления.</span><span class="sxs-lookup"><span data-stu-id="c5e7a-116">Name of the compute policy to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ComputePolicyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5e7a-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c5e7a-117">-PassThru</span></span>
<span data-ttu-id="c5e7a-118">При успешном удалении возвращает значение "истина".</span><span class="sxs-lookup"><span data-stu-id="c5e7a-118">Return true upon successful deletion.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5e7a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5e7a-119">-ResourceGroupName</span></span>
<span data-ttu-id="c5e7a-120">Имя группы ресурсов, в которой есть учетная запись.</span><span class="sxs-lookup"><span data-stu-id="c5e7a-120">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="c5e7a-121">Необязательный и пытается выяснить, не было ли оно указано.</span><span class="sxs-lookup"><span data-stu-id="c5e7a-121">Optional and will attempt to discover if not provided.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5e7a-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c5e7a-122">-Confirm</span></span>
<span data-ttu-id="c5e7a-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c5e7a-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5e7a-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5e7a-124">-WhatIf</span></span>
<span data-ttu-id="c5e7a-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c5e7a-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c5e7a-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c5e7a-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5e7a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5e7a-127">CommonParameters</span></span>
<span data-ttu-id="c5e7a-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c5e7a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5e7a-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5e7a-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5e7a-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c5e7a-130">INPUTS</span></span>

### <span data-ttu-id="c5e7a-131">System. String</span><span class="sxs-lookup"><span data-stu-id="c5e7a-131">System.String</span></span>

## <span data-ttu-id="c5e7a-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c5e7a-132">OUTPUTS</span></span>

### <span data-ttu-id="c5e7a-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c5e7a-133">System.Boolean</span></span>

## <span data-ttu-id="c5e7a-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="c5e7a-134">NOTES</span></span>

## <span data-ttu-id="c5e7a-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c5e7a-135">RELATED LINKS</span></span>

