---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/get-azurermstorageaccountnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageAccountNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageAccountNetworkRuleSet.md
ms.openlocfilehash: 0a316ee8e4d1d7c8d58e2444aa6cdfadbc5e0367
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563931"
---
# <span data-ttu-id="038f2-101">Get-AzureRmStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="038f2-101">Get-AzureRmStorageAccountNetworkRuleSet</span></span>

## <span data-ttu-id="038f2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="038f2-102">SYNOPSIS</span></span>
<span data-ttu-id="038f2-103">Получение свойства NetWorkRule учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="038f2-103">Get the NetWorkRule property of a Storage account</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="038f2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="038f2-104">SYNTAX</span></span>

```
Get-AzureRmStorageAccountNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="038f2-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="038f2-105">DESCRIPTION</span></span>
<span data-ttu-id="038f2-106">Командлет **Get-AzureRmStorageAccountNetworkRuleSet** получает свойство NetworkRule учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="038f2-106">The **Get-AzureRmStorageAccountNetworkRuleSet** cmdlet gets the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="038f2-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="038f2-107">EXAMPLES</span></span>

### <span data-ttu-id="038f2-108">Пример 1: получение свойства NetworkRule для указанной учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="038f2-108">Example 1: Get NetworkRule property of a specified Storage account</span></span>
```
PS C:\> Get-AzureRmStorageAccountNetworkRuleSet  -ResourceGroupName "rg1" -AccountName "mystorageaccount"
```

<span data-ttu-id="038f2-109">Эта команда получает свойство NetworkRule для указанной учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="038f2-109">This command gets NetworkRule property of a specified Storage account</span></span>

## <span data-ttu-id="038f2-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="038f2-110">PARAMETERS</span></span>

### <span data-ttu-id="038f2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="038f2-111">-DefaultProfile</span></span>
<span data-ttu-id="038f2-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="038f2-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="038f2-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="038f2-113">-Name</span></span>
<span data-ttu-id="038f2-114">Указывает имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="038f2-114">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="038f2-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="038f2-115">-ResourceGroupName</span></span>
<span data-ttu-id="038f2-116">Указывает, что имя группы ресурсов содержит учетную запись хранения.</span><span class="sxs-lookup"><span data-stu-id="038f2-116">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="038f2-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="038f2-117">CommonParameters</span></span>
<span data-ttu-id="038f2-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="038f2-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="038f2-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="038f2-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="038f2-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="038f2-120">INPUTS</span></span>

### <span data-ttu-id="038f2-121">System. String</span><span class="sxs-lookup"><span data-stu-id="038f2-121">System.String</span></span>

## <span data-ttu-id="038f2-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="038f2-122">OUTPUTS</span></span>

### <span data-ttu-id="038f2-123">Microsoft. Azure. Commands. Management. Storage. Models. PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="038f2-123">Microsoft.Azure.Commands.Management.Storage.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="038f2-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="038f2-124">NOTES</span></span>

## <span data-ttu-id="038f2-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="038f2-125">RELATED LINKS</span></span>
