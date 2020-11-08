---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageaccountnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountNetworkRuleSet.md
ms.openlocfilehash: e9ce7a0ab98251b86990db5623b91b3a62a4cdcc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236554"
---
# <span data-ttu-id="ce332-101">Get-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="ce332-101">Get-AzStorageAccountNetworkRuleSet</span></span>

## <span data-ttu-id="ce332-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ce332-102">SYNOPSIS</span></span>
<span data-ttu-id="ce332-103">Получение свойства NetWorkRule учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="ce332-103">Get the NetWorkRule property of a Storage account</span></span>

## <span data-ttu-id="ce332-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ce332-104">SYNTAX</span></span>

```
Get-AzStorageAccountNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ce332-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ce332-105">DESCRIPTION</span></span>
<span data-ttu-id="ce332-106">Командлет **Get-AzStorageAccountNetworkRuleSet** получает свойство NetworkRule учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="ce332-106">The **Get-AzStorageAccountNetworkRuleSet** cmdlet gets the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="ce332-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ce332-107">EXAMPLES</span></span>

### <span data-ttu-id="ce332-108">Пример 1: получение свойства NetworkRule для указанной учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="ce332-108">Example 1: Get NetworkRule property of a specified Storage account</span></span>
```
PS C:\> Get-AzStorageAccountNetworkRuleSet  -ResourceGroupName "rg1" -AccountName "mystorageaccount"
```

<span data-ttu-id="ce332-109">Эта команда получает свойство NetworkRule для указанной учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="ce332-109">This command gets NetworkRule property of a specified Storage account</span></span>

## <span data-ttu-id="ce332-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ce332-110">PARAMETERS</span></span>

### <span data-ttu-id="ce332-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce332-111">-DefaultProfile</span></span>
<span data-ttu-id="ce332-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ce332-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ce332-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ce332-113">-Name</span></span>
<span data-ttu-id="ce332-114">Указывает имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="ce332-114">Specifies the name of the Storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce332-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce332-115">-ResourceGroupName</span></span>
<span data-ttu-id="ce332-116">Указывает, что имя группы ресурсов содержит учетную запись хранения.</span><span class="sxs-lookup"><span data-stu-id="ce332-116">Specifies the name of the resource group contains the Storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce332-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce332-117">CommonParameters</span></span>
<span data-ttu-id="ce332-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ce332-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce332-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce332-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce332-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ce332-120">INPUTS</span></span>

### <span data-ttu-id="ce332-121">System. String</span><span class="sxs-lookup"><span data-stu-id="ce332-121">System.String</span></span>

## <span data-ttu-id="ce332-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ce332-122">OUTPUTS</span></span>

### <span data-ttu-id="ce332-123">Microsoft. Azure. Commands. Management. Storage. Models. PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="ce332-123">Microsoft.Azure.Commands.Management.Storage.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="ce332-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="ce332-124">NOTES</span></span>

## <span data-ttu-id="ce332-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ce332-125">RELATED LINKS</span></span>