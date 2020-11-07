---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/get-azurermstorageaccountnetworkruleset
schema: 2.0.0
ms.openlocfilehash: 8e3aa3bd313947712ef3831b83c75bb1349adb4f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913722"
---
# <span data-ttu-id="b8205-101">Get-AzureRmStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="b8205-101">Get-AzureRmStorageAccountNetworkRuleSet</span></span>

## <span data-ttu-id="b8205-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b8205-102">SYNOPSIS</span></span>
<span data-ttu-id="b8205-103">Получение свойства NetWorkRule учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="b8205-103">Get the NetWorkRule property of a Storage account</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b8205-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b8205-104">SYNTAX</span></span>

```
Get-AzureRmStorageAccountNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b8205-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b8205-105">DESCRIPTION</span></span>
<span data-ttu-id="b8205-106">Командлет **Get-AzureRmStorageAccountNetworkRuleSet** получает свойство NetworkRule учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="b8205-106">The **Get-AzureRmStorageAccountNetworkRuleSet** cmdlet gets the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="b8205-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b8205-107">EXAMPLES</span></span>

### <span data-ttu-id="b8205-108">Пример 1: получение свойства NetworkRule для указанной учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="b8205-108">Example 1: Get NetworkRule property of a specified Storage account</span></span>
```
PS C:\> Get-AzureRmStorageAccountNetworkRuleSet  -ResourceGroupName "rg1" -AccountName "mystorageaccount"
```

<span data-ttu-id="b8205-109">Эта команда получает свойство NetworkRule для указанной учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="b8205-109">This command gets NetworkRule property of a specified Storage account</span></span>

## <span data-ttu-id="b8205-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b8205-110">PARAMETERS</span></span>

### <span data-ttu-id="b8205-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8205-111">-DefaultProfile</span></span>
<span data-ttu-id="b8205-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b8205-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b8205-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b8205-113">-Name</span></span>
<span data-ttu-id="b8205-114">Указывает имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="b8205-114">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="b8205-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8205-115">-ResourceGroupName</span></span>
<span data-ttu-id="b8205-116">Указывает, что имя группы ресурсов содержит учетную запись хранения.</span><span class="sxs-lookup"><span data-stu-id="b8205-116">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="b8205-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8205-117">CommonParameters</span></span>
<span data-ttu-id="b8205-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b8205-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8205-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8205-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8205-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b8205-120">INPUTS</span></span>

### <span data-ttu-id="b8205-121">System. String</span><span class="sxs-lookup"><span data-stu-id="b8205-121">System.String</span></span>

## <span data-ttu-id="b8205-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b8205-122">OUTPUTS</span></span>

### <span data-ttu-id="b8205-123">Microsoft. Azure. Commands. Management. Storage. Models. PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="b8205-123">Microsoft.Azure.Commands.Management.Storage.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="b8205-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="b8205-124">NOTES</span></span>

## <span data-ttu-id="b8205-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b8205-125">RELATED LINKS</span></span>
