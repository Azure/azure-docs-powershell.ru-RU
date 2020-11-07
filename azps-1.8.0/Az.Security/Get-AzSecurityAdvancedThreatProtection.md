---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/get-azsecurityadvancedthreatprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdvancedThreatProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdvancedThreatProtection.md
ms.openlocfilehash: 8957a794660750f45f295b77d921e647d368e7dc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93729258"
---
# <span data-ttu-id="f7e86-101">Get-AzSecurityAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="f7e86-101">Get-AzSecurityAdvancedThreatProtection</span></span>

## <span data-ttu-id="f7e86-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f7e86-102">SYNOPSIS</span></span>
<span data-ttu-id="f7e86-103">Получает расширенную политику защиты от угроз для учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="f7e86-103">Gets the advanced threat protection policy for a storage account.</span></span>

## <span data-ttu-id="f7e86-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f7e86-104">SYNTAX</span></span>

```
Get-AzSecurityAdvancedThreatProtection -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f7e86-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f7e86-105">DESCRIPTION</span></span>
<span data-ttu-id="f7e86-106">`Get-AzSecurityAdvancedThreatProtection`Командлет получает политику защиты от угроз для учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="f7e86-106">The `Get-AzSecurityAdvancedThreatProtection` cmdlet gets the threat protection policy for a storage account.</span></span>
<span data-ttu-id="f7e86-107">Чтобы использовать этот командлет, укажите параметр *ResourceId* .</span><span class="sxs-lookup"><span data-stu-id="f7e86-107">To use this cmdlet, specify the *ResourceId* parameter.</span></span>

## <span data-ttu-id="f7e86-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f7e86-108">EXAMPLES</span></span>

### <span data-ttu-id="f7e86-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f7e86-109">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"

IsEnabled Id
--------- --
    False  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"
```

<span data-ttu-id="f7e86-110">Эта команда получает расширенную политику защиты от угроз для идентификатора ресурса `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"` .</span><span class="sxs-lookup"><span data-stu-id="f7e86-110">This command gets the advanced threat protection policy for resource id `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"`.</span></span>

## <span data-ttu-id="f7e86-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f7e86-111">PARAMETERS</span></span>

### <span data-ttu-id="f7e86-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7e86-112">-DefaultProfile</span></span>
<span data-ttu-id="f7e86-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f7e86-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7e86-114">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f7e86-114">-ResourceId</span></span>
<span data-ttu-id="f7e86-115">Идентификатор ресурса безопасности, для которого нужно вызвать команду.</span><span class="sxs-lookup"><span data-stu-id="f7e86-115">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="f7e86-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7e86-116">CommonParameters</span></span>
<span data-ttu-id="f7e86-117">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f7e86-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7e86-118">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7e86-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7e86-119">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f7e86-119">INPUTS</span></span>

### <span data-ttu-id="f7e86-120">System. String</span><span class="sxs-lookup"><span data-stu-id="f7e86-120">System.String</span></span>

## <span data-ttu-id="f7e86-121">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f7e86-121">OUTPUTS</span></span>

### <span data-ttu-id="f7e86-122">Microsoft. Azure. Commands. Security. Models. AdvancedThreatProtection. PSAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="f7e86-122">Microsoft.Azure.Commands.Security.Models.AdvancedThreatProtection.PSAdvancedThreatProtection</span></span>

## <span data-ttu-id="f7e86-123">Пуск</span><span class="sxs-lookup"><span data-stu-id="f7e86-123">NOTES</span></span>

## <span data-ttu-id="f7e86-124">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f7e86-124">RELATED LINKS</span></span>
