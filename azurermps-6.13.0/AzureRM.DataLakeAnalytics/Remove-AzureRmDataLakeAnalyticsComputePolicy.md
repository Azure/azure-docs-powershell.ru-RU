---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/remove-azurermdatalakeanalyticscomputepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: a97c6835144cda227fc07645f087e393cda2b8f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560943"
---
# <span data-ttu-id="83188-101">Remove-AzureRmDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="83188-101">Remove-AzureRmDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="83188-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="83188-102">SYNOPSIS</span></span>
<span data-ttu-id="83188-103">Удаляет указанную политику вычисления данных Azure Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="83188-103">Removes a specified Azure Data Lake Analytics compute policy</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="83188-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="83188-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [-Name] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="83188-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="83188-105">DESCRIPTION</span></span>
<span data-ttu-id="83188-106">Параметр **Remove-AzureRmDataLakeAnalyticsComputePolicy** удаляет указанную политику вычисления Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="83188-106">The **Remove-AzureRmDataLakeAnalyticsComputePolicy** removes a specified Azure Data Lake Analytics compute policy.</span></span>

## <span data-ttu-id="83188-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="83188-107">EXAMPLES</span></span>

### <span data-ttu-id="83188-108">Пример 1: Удаление политики вычислений</span><span class="sxs-lookup"><span data-stu-id="83188-108">Example 1: Remove a compute policy</span></span>
```
PS C:\>Remove-AzureRmDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name myPolicy
```

<span data-ttu-id="83188-109">Эта команда удаляет указанную политику вычислений с именем "myPolicy" в учетной записи "contosoadla".</span><span class="sxs-lookup"><span data-stu-id="83188-109">This command removes the specified compute policy with name 'myPolicy' in account 'contosoadla'.</span></span>

## <span data-ttu-id="83188-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="83188-110">PARAMETERS</span></span>

### <span data-ttu-id="83188-111">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="83188-111">-Account</span></span>
<span data-ttu-id="83188-112">Имя учетной записи, из которой нужно удалить политику вычислений.</span><span class="sxs-lookup"><span data-stu-id="83188-112">Name of the account to remove the compute policy from.</span></span>

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

### <span data-ttu-id="83188-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83188-113">-DefaultProfile</span></span>
<span data-ttu-id="83188-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="83188-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="83188-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="83188-115">-Name</span></span>
<span data-ttu-id="83188-116">Имя удаляемой политики вычисления.</span><span class="sxs-lookup"><span data-stu-id="83188-116">Name of the compute policy to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ComputePolicyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83188-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="83188-117">-PassThru</span></span>
<span data-ttu-id="83188-118">При успешном удалении возвращает значение "истина".</span><span class="sxs-lookup"><span data-stu-id="83188-118">Return true upon successful deletion.</span></span>

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

### <span data-ttu-id="83188-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83188-119">-ResourceGroupName</span></span>
<span data-ttu-id="83188-120">Имя группы ресурсов, в которой есть учетная запись.</span><span class="sxs-lookup"><span data-stu-id="83188-120">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="83188-121">Необязательный и пытается выяснить, не было ли оно указано.</span><span class="sxs-lookup"><span data-stu-id="83188-121">Optional and will attempt to discover if not provided.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83188-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="83188-122">-Confirm</span></span>
<span data-ttu-id="83188-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="83188-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83188-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83188-124">-WhatIf</span></span>
<span data-ttu-id="83188-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="83188-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="83188-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="83188-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="83188-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83188-127">CommonParameters</span></span>
<span data-ttu-id="83188-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="83188-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83188-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83188-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83188-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="83188-130">INPUTS</span></span>

### <span data-ttu-id="83188-131">System. String</span><span class="sxs-lookup"><span data-stu-id="83188-131">System.String</span></span>

## <span data-ttu-id="83188-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="83188-132">OUTPUTS</span></span>

### <span data-ttu-id="83188-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="83188-133">System.Boolean</span></span>

## <span data-ttu-id="83188-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="83188-134">NOTES</span></span>

## <span data-ttu-id="83188-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="83188-135">RELATED LINKS</span></span>
