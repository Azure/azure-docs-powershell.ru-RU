---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 30C10687-F172-4663-8D4A-F0DDEA5C3741
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: 089dbc5e3ca1d6a4a2a6528cb0c4bc87cf9b3dad
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93570424"
---
# <span data-ttu-id="8fa2b-101">Remove-AzureRmDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="8fa2b-101">Remove-AzureRmDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="8fa2b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8fa2b-102">SYNOPSIS</span></span>
<span data-ttu-id="8fa2b-103">Удаляет указанного доверенного поставщика удостоверений в указанном Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="8fa2b-103">Removes the specified trusted identity provider in the specified Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8fa2b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8fa2b-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeStoreTrustedIdProvider [-Account] <String> [[-Name] <String>] [-PassThru]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8fa2b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8fa2b-105">DESCRIPTION</span></span>
<span data-ttu-id="8fa2b-106">Командлет **Remove-AzureRmDataLakeStoreTrustedIdProvider** Удаляет указанного доверенного поставщика удостоверений в указанном Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="8fa2b-106">The **Remove-AzureRmDataLakeStoreTrustedIdProvider** cmdlet removes the specified trusted identity provider in the specified Data Lake Store.</span></span>

## <span data-ttu-id="8fa2b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8fa2b-107">EXAMPLES</span></span>

### <span data-ttu-id="8fa2b-108">Пример 1: Удаление надежного поставщика удостоверений.</span><span class="sxs-lookup"><span data-stu-id="8fa2b-108">Example 1: Remove a trusted identity provider.</span></span>
```
PS C:\> Remove-AzureRmDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider
```

<span data-ttu-id="8fa2b-109">Удаление поставщика "MyProvider" из учетной записи "ContosoADL"</span><span class="sxs-lookup"><span data-stu-id="8fa2b-109">Removes the provider "MyProvider" from account "ContosoADL"</span></span>

## <span data-ttu-id="8fa2b-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8fa2b-110">PARAMETERS</span></span>

### <span data-ttu-id="8fa2b-111">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="8fa2b-111">-Account</span></span>
<span data-ttu-id="8fa2b-112">Учетная запись Data Lake Store для удаления доверенного поставщика удостоверений из</span><span class="sxs-lookup"><span data-stu-id="8fa2b-112">The Data Lake Store account to remove the trusted identity provider from</span></span>

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

### <span data-ttu-id="8fa2b-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8fa2b-113">-Name</span></span>
<span data-ttu-id="8fa2b-114">Имя надежного поставщика удостоверений.</span><span class="sxs-lookup"><span data-stu-id="8fa2b-114">The name of the trusted identity provider.</span></span>

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

### <span data-ttu-id="8fa2b-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8fa2b-115">-PassThru</span></span>
<span data-ttu-id="8fa2b-116">Указывает, что должен возвращаться логический ответ, указывающий результат операции удаления.</span><span class="sxs-lookup"><span data-stu-id="8fa2b-116">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="8fa2b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8fa2b-117">-ResourceGroupName</span></span>
<span data-ttu-id="8fa2b-118">Указывает имя группы ресурсов, которая содержит учетную запись, из которой нужно удалить доверенный поставщик удостоверений.</span><span class="sxs-lookup"><span data-stu-id="8fa2b-118">Specifies the name of the resource group that contains the account to remove the trusted identity provider from.</span></span>

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

### <span data-ttu-id="8fa2b-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8fa2b-119">-Confirm</span></span>
<span data-ttu-id="8fa2b-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8fa2b-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8fa2b-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8fa2b-121">-WhatIf</span></span>
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

### <span data-ttu-id="8fa2b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fa2b-122">-DefaultProfile</span></span>
<span data-ttu-id="8fa2b-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8fa2b-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8fa2b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fa2b-124">CommonParameters</span></span>
<span data-ttu-id="8fa2b-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8fa2b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fa2b-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8fa2b-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fa2b-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8fa2b-127">INPUTS</span></span>

## <span data-ttu-id="8fa2b-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8fa2b-128">OUTPUTS</span></span>

### <span data-ttu-id="8fa2b-129">логических</span><span class="sxs-lookup"><span data-stu-id="8fa2b-129">bool</span></span>
<span data-ttu-id="8fa2b-130">Если указана функция PassThru, при успешном завершении возвращает значение истина.</span><span class="sxs-lookup"><span data-stu-id="8fa2b-130">If PassThru is specified, returns true upon successful completion.</span></span>

## <span data-ttu-id="8fa2b-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="8fa2b-131">NOTES</span></span>

## <span data-ttu-id="8fa2b-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8fa2b-132">RELATED LINKS</span></span>

