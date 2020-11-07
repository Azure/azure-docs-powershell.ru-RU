---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/get-azurermdefault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmDefault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmDefault.md
ms.openlocfilehash: 7430402d62d88ea192b94166f48c0657e47cbf15
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732238"
---
# <span data-ttu-id="32107-101">Get-AzureRmDefault</span><span class="sxs-lookup"><span data-stu-id="32107-101">Get-AzureRmDefault</span></span>

## <span data-ttu-id="32107-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="32107-102">SYNOPSIS</span></span>
<span data-ttu-id="32107-103">Получение значений по умолчанию, заданных пользователем в текущем контексте.</span><span class="sxs-lookup"><span data-stu-id="32107-103">Get the defaults set by the user in the current context.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="32107-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="32107-104">SYNTAX</span></span>

```
Get-AzureRmDefault [-ResourceGroup] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="32107-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="32107-105">DESCRIPTION</span></span>
<span data-ttu-id="32107-106">Командлет Get-AzureRmDefault получает группу ресурсов, которую пользователь задали в качестве значения по умолчанию в текущем контексте.</span><span class="sxs-lookup"><span data-stu-id="32107-106">The Get-AzureRmDefault cmdlet gets the Resource Group that the user has set as default in the current context.</span></span>

## <span data-ttu-id="32107-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="32107-107">EXAMPLES</span></span>

### <span data-ttu-id="32107-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="32107-108">Example 1</span></span>
```
PS C:\> Get-AzureRmDefault

Id         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myResourceGroup
Name       : myResourceGroup
Properties : Microsoft.Azure.Management.Internal.Resources.Models.ResourceGroupProperties
Location   : eastus
ManagedBy  :
Tags       :
```

<span data-ttu-id="32107-109">Эта команда возвращает текущие значения по умолчанию, если заданы значения по умолчанию, или значение Nothing, если не задано значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="32107-109">This command returns the current defaults if there are defaults set, or returns nothing if no default is set.</span></span>

### <span data-ttu-id="32107-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="32107-110">Example 2</span></span>
```
PS C:\> Get-AzureRmDefault -ResourceGroup

Id         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myResourceGroup
Name       : myResourceGroup
Properties : Microsoft.Azure.Management.Internal.Resources.Models.ResourceGroupProperties
Location   : eastus
ManagedBy  :
Tags       :
```

<span data-ttu-id="32107-111">Эта команда возвращает текущую группу ресурсов по умолчанию, если задано значение по умолчанию, или значение Nothing, если не задано значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="32107-111">This command returns the current default Resource Group if there is a default set, or returns nothing if no default is set.</span></span>

## <span data-ttu-id="32107-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="32107-112">PARAMETERS</span></span>

### <span data-ttu-id="32107-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32107-113">-DefaultProfile</span></span>
<span data-ttu-id="32107-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="32107-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="32107-115">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="32107-115">-ResourceGroup</span></span>
<span data-ttu-id="32107-116">Отображение группы ресурсов по умолчанию</span><span class="sxs-lookup"><span data-stu-id="32107-116">Display Default Resource Group</span></span>

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

### <span data-ttu-id="32107-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32107-117">CommonParameters</span></span>
<span data-ttu-id="32107-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="32107-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32107-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32107-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32107-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="32107-120">INPUTS</span></span>

### <span data-ttu-id="32107-121">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="32107-121">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="32107-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="32107-122">OUTPUTS</span></span>

### <span data-ttu-id="32107-123">Microsoft. Azure. Commands. Profile. Models. PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="32107-123">Microsoft.Azure.Commands.Profile.Models.PSResourceGroup</span></span>

## <span data-ttu-id="32107-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="32107-124">NOTES</span></span>

## <span data-ttu-id="32107-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="32107-125">RELATED LINKS</span></span>
