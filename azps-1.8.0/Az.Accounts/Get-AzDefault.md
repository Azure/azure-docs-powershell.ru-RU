---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azdefault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzDefault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzDefault.md
ms.openlocfilehash: 374a43b6b094622808f4704daf7063a4c4c0c153
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720268"
---
# <span data-ttu-id="71624-101">Get-AzDefault</span><span class="sxs-lookup"><span data-stu-id="71624-101">Get-AzDefault</span></span>

## <span data-ttu-id="71624-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="71624-102">SYNOPSIS</span></span>
<span data-ttu-id="71624-103">Получение значений по умолчанию, заданных пользователем в текущем контексте.</span><span class="sxs-lookup"><span data-stu-id="71624-103">Get the defaults set by the user in the current context.</span></span>

## <span data-ttu-id="71624-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="71624-104">SYNTAX</span></span>

```
Get-AzDefault [-ResourceGroup] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="71624-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="71624-105">DESCRIPTION</span></span>
<span data-ttu-id="71624-106">Командлет Get-AzDefault получает группу ресурсов, которую пользователь задали в качестве значения по умолчанию в текущем контексте.</span><span class="sxs-lookup"><span data-stu-id="71624-106">The Get-AzDefault cmdlet gets the Resource Group that the user has set as default in the current context.</span></span>

## <span data-ttu-id="71624-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="71624-107">EXAMPLES</span></span>

### <span data-ttu-id="71624-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="71624-108">Example 1</span></span>
```
PS C:\> Get-AzDefault

Id         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myResourceGroup
Name       : myResourceGroup
Properties : Microsoft.Azure.Management.Internal.Resources.Models.ResourceGroupProperties
Location   : eastus
ManagedBy  :
Tags       :
```

<span data-ttu-id="71624-109">Эта команда возвращает текущие значения по умолчанию, если заданы значения по умолчанию, или значение Nothing, если не задано значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="71624-109">This command returns the current defaults if there are defaults set, or returns nothing if no default is set.</span></span>

### <span data-ttu-id="71624-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="71624-110">Example 2</span></span>
```
PS C:\> Get-AzDefault -ResourceGroup

Id         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myResourceGroup
Name       : myResourceGroup
Properties : Microsoft.Azure.Management.Internal.Resources.Models.ResourceGroupProperties
Location   : eastus
ManagedBy  :
Tags       :
```

<span data-ttu-id="71624-111">Эта команда возвращает текущую группу ресурсов по умолчанию, если задано значение по умолчанию, или значение Nothing, если не задано значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="71624-111">This command returns the current default Resource Group if there is a default set, or returns nothing if no default is set.</span></span>

## <span data-ttu-id="71624-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="71624-112">PARAMETERS</span></span>

### <span data-ttu-id="71624-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71624-113">-DefaultProfile</span></span>
<span data-ttu-id="71624-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="71624-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="71624-115">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="71624-115">-ResourceGroup</span></span>
<span data-ttu-id="71624-116">Отображение группы ресурсов по умолчанию</span><span class="sxs-lookup"><span data-stu-id="71624-116">Display Default Resource Group</span></span>

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

### <span data-ttu-id="71624-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71624-117">CommonParameters</span></span>
<span data-ttu-id="71624-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="71624-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71624-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71624-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71624-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="71624-120">INPUTS</span></span>

### <span data-ttu-id="71624-121">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="71624-121">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="71624-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="71624-122">OUTPUTS</span></span>

### <span data-ttu-id="71624-123">Microsoft. Azure. Commands. Profile. Models. PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="71624-123">Microsoft.Azure.Commands.Profile.Models.PSResourceGroup</span></span>

## <span data-ttu-id="71624-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="71624-124">NOTES</span></span>

## <span data-ttu-id="71624-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="71624-125">RELATED LINKS</span></span>
