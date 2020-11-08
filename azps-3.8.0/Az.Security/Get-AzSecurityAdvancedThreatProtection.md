---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/get-azsecurityadvancedthreatprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdvancedThreatProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdvancedThreatProtection.md
ms.openlocfilehash: d4d2ae2ae8b09f319efe2f77030c88338b4c40b9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074307"
---
# <span data-ttu-id="2ebab-101">Get-AzSecurityAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="2ebab-101">Get-AzSecurityAdvancedThreatProtection</span></span>

## <span data-ttu-id="2ebab-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2ebab-102">SYNOPSIS</span></span>
<span data-ttu-id="2ebab-103">Получает расширенную политику защиты от угроз для учетной записи хранилища и cosmosDB.</span><span class="sxs-lookup"><span data-stu-id="2ebab-103">Gets the advanced threat protection policy for a storage / cosmosDB account.</span></span>

## <span data-ttu-id="2ebab-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2ebab-104">SYNTAX</span></span>

```
Get-AzSecurityAdvancedThreatProtection -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2ebab-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2ebab-105">DESCRIPTION</span></span>
<span data-ttu-id="2ebab-106">`Get-AzSecurityAdvancedThreatProtection`Командлет получает политику защиты от угроз для учетной записи хранилища и cosmosDB.</span><span class="sxs-lookup"><span data-stu-id="2ebab-106">The `Get-AzSecurityAdvancedThreatProtection` cmdlet gets the threat protection policy for a storage / cosmosDB account.</span></span>
<span data-ttu-id="2ebab-107">Чтобы использовать этот командлет, укажите параметр *ResourceId* .</span><span class="sxs-lookup"><span data-stu-id="2ebab-107">To use this cmdlet, specify the *ResourceId* parameter.</span></span>

## <span data-ttu-id="2ebab-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2ebab-108">EXAMPLES</span></span>

### <span data-ttu-id="2ebab-109">Пример 1: учетная запись хранения</span><span class="sxs-lookup"><span data-stu-id="2ebab-109">Example 1 : Storage Account</span></span>
```powershell
PS C:\> Get-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"

IsEnabled Id
--------- --
    False  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"
```

<span data-ttu-id="2ebab-110">Эта команда получает расширенную политику защиты от угроз для идентификатора ресурса `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"` .</span><span class="sxs-lookup"><span data-stu-id="2ebab-110">This command gets the advanced threat protection policy for resource id `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"`.</span></span>

### <span data-ttu-id="2ebab-111">Пример 2: учетная запись CosmosDB</span><span class="sxs-lookup"><span data-stu-id="2ebab-111">Example 2 : CosmosDB Account</span></span>
```powershell
PS C:\> Get-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"

IsEnabled Id
--------- --
    True  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"
```
<span data-ttu-id="2ebab-112">Эта команда получает расширенную политику защиты от угроз для идентификатора ресурса ` "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"` .</span><span class="sxs-lookup"><span data-stu-id="2ebab-112">This command gets the advanced threat protection policy for resource id ` "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"`.</span></span>


## <span data-ttu-id="2ebab-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2ebab-113">PARAMETERS</span></span>

### <span data-ttu-id="2ebab-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ebab-114">-DefaultProfile</span></span>
<span data-ttu-id="2ebab-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2ebab-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ebab-116">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2ebab-116">-ResourceId</span></span>
<span data-ttu-id="2ebab-117">Идентификатор ресурса безопасности, для которого нужно вызвать команду.</span><span class="sxs-lookup"><span data-stu-id="2ebab-117">ID of the security resource that you want to invoke the command on.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ebab-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ebab-118">CommonParameters</span></span>
<span data-ttu-id="2ebab-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2ebab-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ebab-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ebab-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ebab-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2ebab-121">INPUTS</span></span>

### <span data-ttu-id="2ebab-122">System. String</span><span class="sxs-lookup"><span data-stu-id="2ebab-122">System.String</span></span>

## <span data-ttu-id="2ebab-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2ebab-123">OUTPUTS</span></span>

### <span data-ttu-id="2ebab-124">Microsoft. Azure. Commands. Security. Models. AdvancedThreatProtection. PSAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="2ebab-124">Microsoft.Azure.Commands.Security.Models.AdvancedThreatProtection.PSAdvancedThreatProtection</span></span>

## <span data-ttu-id="2ebab-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="2ebab-125">NOTES</span></span>

## <span data-ttu-id="2ebab-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2ebab-126">RELATED LINKS</span></span>
