---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 30C10687-F172-4663-8D4A-F0DDEA5C3741
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/remove-azdatalakestoretrustedidprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: 3e16db29f6560778dff5c86ac222d06fd41a5807
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98504563"
---
# <span data-ttu-id="d254a-101">Remove-AzDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="d254a-101">Remove-AzDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="d254a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d254a-102">SYNOPSIS</span></span>
<span data-ttu-id="d254a-103">Удаление указанного надежного поставщика удостоверений из указанного магазина Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="d254a-103">Removes the specified trusted identity provider in the specified Data Lake Store.</span></span>

## <span data-ttu-id="d254a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d254a-104">SYNTAX</span></span>

```
Remove-AzDataLakeStoreTrustedIdProvider [-Account] <String> [[-Name] <String>] [-PassThru]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d254a-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d254a-105">DESCRIPTION</span></span>
<span data-ttu-id="d254a-106">Для удаления указанного надежного поставщика удостоверений из указанного магазина Data Lake Store удаляется **cmdlet Remove-AzDataLakeStoreTrustedIdProvider.**</span><span class="sxs-lookup"><span data-stu-id="d254a-106">The **Remove-AzDataLakeStoreTrustedIdProvider** cmdlet removes the specified trusted identity provider in the specified Data Lake Store.</span></span>

## <span data-ttu-id="d254a-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d254a-107">EXAMPLES</span></span>

### <span data-ttu-id="d254a-108">Пример 1. Удаление надежного поставщика удостоверений.</span><span class="sxs-lookup"><span data-stu-id="d254a-108">Example 1: Remove a trusted identity provider.</span></span>
```
PS C:\> Remove-AzDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider
```

<span data-ttu-id="d254a-109">Удаление поставщика "MyProvider" из учетной записи ContosoADL</span><span class="sxs-lookup"><span data-stu-id="d254a-109">Removes the provider "MyProvider" from account "ContosoADL"</span></span>

## <span data-ttu-id="d254a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d254a-110">PARAMETERS</span></span>

### <span data-ttu-id="d254a-111">-Account</span><span class="sxs-lookup"><span data-stu-id="d254a-111">-Account</span></span>
<span data-ttu-id="d254a-112">Учетная запись Data Lake Store для удаления надежного поставщика удостоверений из</span><span class="sxs-lookup"><span data-stu-id="d254a-112">The Data Lake Store account to remove the trusted identity provider from</span></span>

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

### <span data-ttu-id="d254a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d254a-113">-DefaultProfile</span></span>
<span data-ttu-id="d254a-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="d254a-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d254a-115">-Name</span><span class="sxs-lookup"><span data-stu-id="d254a-115">-Name</span></span>
<span data-ttu-id="d254a-116">Имя надежного поставщика удостоверений.</span><span class="sxs-lookup"><span data-stu-id="d254a-116">The name of the trusted identity provider.</span></span>

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

### <span data-ttu-id="d254a-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d254a-117">-PassThru</span></span>
<span data-ttu-id="d254a-118">Указывает на то, что должен быть возвращен boolean response, указывающий на результат операции удаления.</span><span class="sxs-lookup"><span data-stu-id="d254a-118">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="d254a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d254a-119">-ResourceGroupName</span></span>
<span data-ttu-id="d254a-120">Имя группы ресурсов, содержаной учетную запись, из которого нужно удалить надежного поставщика удостоверений.</span><span class="sxs-lookup"><span data-stu-id="d254a-120">Specifies the name of the resource group that contains the account to remove the trusted identity provider from.</span></span>

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

### <span data-ttu-id="d254a-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d254a-121">-Confirm</span></span>
<span data-ttu-id="d254a-122">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="d254a-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d254a-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d254a-123">-WhatIf</span></span>
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

### <span data-ttu-id="d254a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d254a-124">CommonParameters</span></span>
<span data-ttu-id="d254a-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d254a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d254a-126">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d254a-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d254a-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d254a-127">INPUTS</span></span>

### <span data-ttu-id="d254a-128">System.String</span><span class="sxs-lookup"><span data-stu-id="d254a-128">System.String</span></span>

### <span data-ttu-id="d254a-129">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="d254a-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="d254a-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d254a-130">OUTPUTS</span></span>

### <span data-ttu-id="d254a-131">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d254a-131">System.Boolean</span></span>

## <span data-ttu-id="d254a-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d254a-132">NOTES</span></span>

## <span data-ttu-id="d254a-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d254a-133">RELATED LINKS</span></span>
