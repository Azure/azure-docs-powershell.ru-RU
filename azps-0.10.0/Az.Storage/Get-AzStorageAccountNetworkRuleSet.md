---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageaccountnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageAccountNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageAccountNetworkRuleSet.md
ms.openlocfilehash: 7cd67b98b91a03e47ecefba7f329655895972913
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910779"
---
# <span data-ttu-id="9a7f3-101">Get-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="9a7f3-101">Get-AzStorageAccountNetworkRuleSet</span></span>

## <span data-ttu-id="9a7f3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9a7f3-102">SYNOPSIS</span></span>
<span data-ttu-id="9a7f3-103">Получение свойства NetWorkRule учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="9a7f3-103">Get the NetWorkRule property of a Storage account</span></span>

## <span data-ttu-id="9a7f3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9a7f3-104">SYNTAX</span></span>

```
Get-AzStorageAccountNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9a7f3-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9a7f3-105">DESCRIPTION</span></span>
<span data-ttu-id="9a7f3-106">Командлет **Get-AzStorageAccountNetworkRuleSet** получает свойство NetworkRule учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="9a7f3-106">The **Get-AzStorageAccountNetworkRuleSet** cmdlet gets the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="9a7f3-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9a7f3-107">EXAMPLES</span></span>

### <span data-ttu-id="9a7f3-108">Пример 1: получение свойства NetworkRule для указанной учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="9a7f3-108">Example 1: Get NetworkRule property of a specified Storage account</span></span>
```
PS C:\> Get-AzStorageAccountNetworkRuleSet  -ResourceGroupName "rg1" -AccountName "mystorageaccount"
```

<span data-ttu-id="9a7f3-109">Эта команда получает свойство NetworkRule для указанной учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="9a7f3-109">This command gets NetworkRule property of a specified Storage account</span></span>

## <span data-ttu-id="9a7f3-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9a7f3-110">PARAMETERS</span></span>

### <span data-ttu-id="9a7f3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a7f3-111">-DefaultProfile</span></span>
<span data-ttu-id="9a7f3-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9a7f3-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9a7f3-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9a7f3-113">-Name</span></span>
<span data-ttu-id="9a7f3-114">Указывает имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="9a7f3-114">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="9a7f3-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a7f3-115">-ResourceGroupName</span></span>
<span data-ttu-id="9a7f3-116">Указывает, что имя группы ресурсов содержит учетную запись хранения.</span><span class="sxs-lookup"><span data-stu-id="9a7f3-116">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="9a7f3-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a7f3-117">CommonParameters</span></span>
<span data-ttu-id="9a7f3-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9a7f3-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a7f3-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a7f3-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a7f3-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9a7f3-120">INPUTS</span></span>

### <span data-ttu-id="9a7f3-121">System. String</span><span class="sxs-lookup"><span data-stu-id="9a7f3-121">System.String</span></span>

## <span data-ttu-id="9a7f3-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9a7f3-122">OUTPUTS</span></span>

### <span data-ttu-id="9a7f3-123">Microsoft. Azure. Commands. Management. Storage. Models. PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="9a7f3-123">Microsoft.Azure.Commands.Management.Storage.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="9a7f3-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="9a7f3-124">NOTES</span></span>

## <span data-ttu-id="9a7f3-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9a7f3-125">RELATED LINKS</span></span>
