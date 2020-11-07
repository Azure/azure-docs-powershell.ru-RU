---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageAccountNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageAccountNetworkRuleSet.md
ms.openlocfilehash: 00447be14fe61b76a4dbb4f62e3393bb76c1ddb8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93735029"
---
# <span data-ttu-id="1e5ae-101">Get-AzureRmStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="1e5ae-101">Get-AzureRmStorageAccountNetworkRuleSet</span></span>

## <span data-ttu-id="1e5ae-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1e5ae-102">SYNOPSIS</span></span>
<span data-ttu-id="1e5ae-103">Получение свойства NetWorkRule учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="1e5ae-103">Get the NetWorkRule property of a Storage Account</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1e5ae-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1e5ae-104">SYNTAX</span></span>

```
Get-AzureRmStorageAccountNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1e5ae-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1e5ae-105">DESCRIPTION</span></span>
<span data-ttu-id="1e5ae-106">Командлет **Get-AzureRmStorageAccountNetworkRuleSet** получает свойство NetworkRule учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="1e5ae-106">The **Get-AzureRmStorageAccountNetworkRuleSet** cmdlet gets the NetworkRule property of a Storage Account</span></span>

## <span data-ttu-id="1e5ae-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1e5ae-107">EXAMPLES</span></span>

### <span data-ttu-id="1e5ae-108">Пример 1: получение свойства NetworkRule для указанной учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="1e5ae-108">Example 1: Get NetworkRule property of a specified storage account</span></span>
```
PS C:\> Get-AzureRmStorageAccountNetworkRuleSet  -ResourceGroupName "rg1" -AccountName "mystorageaccount"
```

<span data-ttu-id="1e5ae-109">Эта команда получает свойство NetworkRule для указанной учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="1e5ae-109">This command gets NetworkRule property of a specified storage account</span></span>

## <span data-ttu-id="1e5ae-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1e5ae-110">PARAMETERS</span></span>

### <span data-ttu-id="1e5ae-111">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1e5ae-111">-Name</span></span>
<span data-ttu-id="1e5ae-112">Указывает имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="1e5ae-112">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="1e5ae-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e5ae-113">-ResourceGroupName</span></span>
<span data-ttu-id="1e5ae-114">Указывает, что имя группы ресурсов содержит учетную запись хранения.</span><span class="sxs-lookup"><span data-stu-id="1e5ae-114">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="1e5ae-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e5ae-115">-DefaultProfile</span></span>
<span data-ttu-id="1e5ae-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1e5ae-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1e5ae-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e5ae-117">CommonParameters</span></span>
<span data-ttu-id="1e5ae-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1e5ae-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e5ae-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e5ae-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e5ae-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1e5ae-120">INPUTS</span></span>

### <span data-ttu-id="1e5ae-121">System. String</span><span class="sxs-lookup"><span data-stu-id="1e5ae-121">System.String</span></span>

## <span data-ttu-id="1e5ae-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1e5ae-122">OUTPUTS</span></span>

### <span data-ttu-id="1e5ae-123">Microsoft. Azure. Commands. Management. Storage. Models. PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="1e5ae-123">Microsoft.Azure.Commands.Management.Storage.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="1e5ae-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="1e5ae-124">NOTES</span></span>

## <span data-ttu-id="1e5ae-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1e5ae-125">RELATED LINKS</span></span>

