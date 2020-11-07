---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 30C10687-F172-4663-8D4A-F0DDEA5C3741
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/remove-azdatalakestoretrustedidprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: a93eb93a02c0ba1f5654258da0405f723e69873d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721289"
---
# <span data-ttu-id="143b0-101">Remove-AzDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="143b0-101">Remove-AzDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="143b0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="143b0-102">SYNOPSIS</span></span>
<span data-ttu-id="143b0-103">Удаляет указанного доверенного поставщика удостоверений в указанном Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="143b0-103">Removes the specified trusted identity provider in the specified Data Lake Store.</span></span>

## <span data-ttu-id="143b0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="143b0-104">SYNTAX</span></span>

```
Remove-AzDataLakeStoreTrustedIdProvider [-Account] <String> [[-Name] <String>] [-PassThru]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="143b0-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="143b0-105">DESCRIPTION</span></span>
<span data-ttu-id="143b0-106">Командлет **Remove-AzDataLakeStoreTrustedIdProvider** Удаляет указанного доверенного поставщика удостоверений в указанном Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="143b0-106">The **Remove-AzDataLakeStoreTrustedIdProvider** cmdlet removes the specified trusted identity provider in the specified Data Lake Store.</span></span>

## <span data-ttu-id="143b0-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="143b0-107">EXAMPLES</span></span>

### <span data-ttu-id="143b0-108">Пример 1: Удаление надежного поставщика удостоверений.</span><span class="sxs-lookup"><span data-stu-id="143b0-108">Example 1: Remove a trusted identity provider.</span></span>
```
PS C:\> Remove-AzDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider
```

<span data-ttu-id="143b0-109">Удаление поставщика "MyProvider" из учетной записи "ContosoADL"</span><span class="sxs-lookup"><span data-stu-id="143b0-109">Removes the provider "MyProvider" from account "ContosoADL"</span></span>

## <span data-ttu-id="143b0-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="143b0-110">PARAMETERS</span></span>

### <span data-ttu-id="143b0-111">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="143b0-111">-Account</span></span>
<span data-ttu-id="143b0-112">Учетная запись Data Lake Store для удаления доверенного поставщика удостоверений из</span><span class="sxs-lookup"><span data-stu-id="143b0-112">The Data Lake Store account to remove the trusted identity provider from</span></span>

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

### <span data-ttu-id="143b0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="143b0-113">-DefaultProfile</span></span>
<span data-ttu-id="143b0-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="143b0-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="143b0-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="143b0-115">-Name</span></span>
<span data-ttu-id="143b0-116">Имя надежного поставщика удостоверений.</span><span class="sxs-lookup"><span data-stu-id="143b0-116">The name of the trusted identity provider.</span></span>

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

### <span data-ttu-id="143b0-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="143b0-117">-PassThru</span></span>
<span data-ttu-id="143b0-118">Указывает, что должен возвращаться логический ответ, указывающий результат операции удаления.</span><span class="sxs-lookup"><span data-stu-id="143b0-118">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="143b0-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="143b0-119">-ResourceGroupName</span></span>
<span data-ttu-id="143b0-120">Указывает имя группы ресурсов, которая содержит учетную запись, из которой нужно удалить доверенный поставщик удостоверений.</span><span class="sxs-lookup"><span data-stu-id="143b0-120">Specifies the name of the resource group that contains the account to remove the trusted identity provider from.</span></span>

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

### <span data-ttu-id="143b0-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="143b0-121">-Confirm</span></span>
<span data-ttu-id="143b0-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="143b0-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="143b0-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="143b0-123">-WhatIf</span></span>
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

### <span data-ttu-id="143b0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="143b0-124">CommonParameters</span></span>
<span data-ttu-id="143b0-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="143b0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="143b0-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="143b0-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="143b0-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="143b0-127">INPUTS</span></span>

### <span data-ttu-id="143b0-128">System. String</span><span class="sxs-lookup"><span data-stu-id="143b0-128">System.String</span></span>

### <span data-ttu-id="143b0-129">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="143b0-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="143b0-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="143b0-130">OUTPUTS</span></span>

### <span data-ttu-id="143b0-131">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="143b0-131">System.Boolean</span></span>

## <span data-ttu-id="143b0-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="143b0-132">NOTES</span></span>

## <span data-ttu-id="143b0-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="143b0-133">RELATED LINKS</span></span>
