---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/disable-azsecurityadvancedthreatprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/DIsable-AzSecurityAdvancedThreatProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/DIsable-AzSecurityAdvancedThreatProtection.md
ms.openlocfilehash: 12cd510a495dbb538532dac95e4388c78e9c6bb5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243329"
---
# <span data-ttu-id="500e3-101">Disable-AzSecurityAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="500e3-101">Disable-AzSecurityAdvancedThreatProtection</span></span>

## <span data-ttu-id="500e3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="500e3-102">SYNOPSIS</span></span>
<span data-ttu-id="500e3-103">Отключение расширенной политики защиты от угроз для учетной записи хранения и cosmosDB.</span><span class="sxs-lookup"><span data-stu-id="500e3-103">Disables the advanced threat protection policy for a storage / cosmosDB account.</span></span>

## <span data-ttu-id="500e3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="500e3-104">SYNTAX</span></span>

```
Disable-AzSecurityAdvancedThreatProtection -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="500e3-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="500e3-105">DESCRIPTION</span></span>
<span data-ttu-id="500e3-106">`Disable-AzSecurityAdvancedThreatProtection`Командлет отключает политику защиты от угроз для учетной записи хранилища и cosmosDB.</span><span class="sxs-lookup"><span data-stu-id="500e3-106">The `Disable-AzSecurityAdvancedThreatProtection` cmdlet disables the threat protection policy for a storage / cosmosDB account.</span></span>
<span data-ttu-id="500e3-107">Чтобы использовать этот командлет, укажите параметр *ResourceId* .</span><span class="sxs-lookup"><span data-stu-id="500e3-107">To use this cmdlet, specify the *ResourceId* parameter.</span></span>

## <span data-ttu-id="500e3-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="500e3-108">EXAMPLES</span></span>

### <span data-ttu-id="500e3-109">Пример 1: учетная запись хранения</span><span class="sxs-lookup"><span data-stu-id="500e3-109">Example 1 : Storage Account</span></span>
```powershell
PS C:\> Disable-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"

IsEnabled Id
--------- --
    False  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"
```

<span data-ttu-id="500e3-110">Эта команда отключает расширенную политику защиты от угроз для идентификатора ресурса `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"` .</span><span class="sxs-lookup"><span data-stu-id="500e3-110">This command disables the advanced threat protection policy for resource id `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"`.</span></span>

### <span data-ttu-id="500e3-111">Пример 2: учетная запись CosmosDB</span><span class="sxs-lookup"><span data-stu-id="500e3-111">Example 2 : CosmosDB Account</span></span>
```powershell
PS C:\> Disable-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"

IsEnabled Id
--------- --
    False  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"
```

<span data-ttu-id="500e3-112">Эта команда отключает расширенную политику защиты от угроз для идентификатора ресурса ` "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"` .</span><span class="sxs-lookup"><span data-stu-id="500e3-112">This command disables the advanced threat protection policy for resource id ` "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"`.</span></span>

## <span data-ttu-id="500e3-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="500e3-113">PARAMETERS</span></span>

### <span data-ttu-id="500e3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="500e3-114">-DefaultProfile</span></span>
<span data-ttu-id="500e3-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="500e3-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="500e3-116">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="500e3-116">-ResourceId</span></span>
<span data-ttu-id="500e3-117">Идентификатор ресурса безопасности, для которого нужно вызвать команду.</span><span class="sxs-lookup"><span data-stu-id="500e3-117">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="500e3-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="500e3-118">-Confirm</span></span>
<span data-ttu-id="500e3-119">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="500e3-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="500e3-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="500e3-120">-WhatIf</span></span>
<span data-ttu-id="500e3-121">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="500e3-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="500e3-122">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="500e3-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="500e3-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="500e3-123">CommonParameters</span></span>
<span data-ttu-id="500e3-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="500e3-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="500e3-125">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="500e3-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="500e3-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="500e3-126">INPUTS</span></span>

### <span data-ttu-id="500e3-127">Ничего</span><span class="sxs-lookup"><span data-stu-id="500e3-127">None</span></span>

## <span data-ttu-id="500e3-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="500e3-128">OUTPUTS</span></span>

### <span data-ttu-id="500e3-129">Microsoft. Azure. Commands. Security. Models. AdvancedThreatProtection. PSAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="500e3-129">Microsoft.Azure.Commands.Security.Models.AdvancedThreatProtection.PSAdvancedThreatProtection</span></span>

## <span data-ttu-id="500e3-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="500e3-130">NOTES</span></span>

## <span data-ttu-id="500e3-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="500e3-131">RELATED LINKS</span></span>