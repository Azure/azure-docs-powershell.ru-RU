---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzProfile.md
ms.openlocfilehash: 937683c8592bb814b7f6a6262ef095cbd8252c78
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93728250"
---
# <span data-ttu-id="e8d0b-101">Get-AzProfile</span><span class="sxs-lookup"><span data-stu-id="e8d0b-101">Get-AzProfile</span></span>

## <span data-ttu-id="e8d0b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e8d0b-102">SYNOPSIS</span></span>
<span data-ttu-id="e8d0b-103">Получение профилей служб, поддерживаемых установленными модулями.</span><span class="sxs-lookup"><span data-stu-id="e8d0b-103">Get the service profiles supported by installed modules.</span></span>

## <span data-ttu-id="e8d0b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e8d0b-104">SYNTAX</span></span>

```
Get-AzProfile [-ModuleName <String[]>] [-ListAvailable] [<CommonParameters>]
```

## <span data-ttu-id="e8d0b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e8d0b-105">DESCRIPTION</span></span>
<span data-ttu-id="e8d0b-106">Получение профилей служб, поддерживаемых установленными модулями.</span><span class="sxs-lookup"><span data-stu-id="e8d0b-106">Get the service profiles supported by installed modules.</span></span>

## <span data-ttu-id="e8d0b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e8d0b-107">EXAMPLES</span></span>

### <span data-ttu-id="e8d0b-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e8d0b-108">Example 1</span></span>
```powershell
PS C:\> Get-AzProfile -ModuleName Az.KeyVault

Name              Description
----              -----------
latest-2019-04-30 A snapshot of the service API versions in the Azure Global Cloud. This profile was defined in April 2019.
hybrid-2019-03-01 A snapshot of the Service API versions in AzureStack, Azure Sovereign clouds, and the Azure Global Cloud. This profile was defined                    in March 2019.
```

<span data-ttu-id="e8d0b-109">Получение профиля службы, поддерживаемого модулем KeyVault</span><span class="sxs-lookup"><span data-stu-id="e8d0b-109">Get the service profile supported by the KeyVault module</span></span>

## <span data-ttu-id="e8d0b-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e8d0b-110">PARAMETERS</span></span>

### <span data-ttu-id="e8d0b-111">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="e8d0b-111">-ListAvailable</span></span>
<span data-ttu-id="e8d0b-112">Список всех профилей служб, поддерживаемых установленными модулями</span><span class="sxs-lookup"><span data-stu-id="e8d0b-112">List all service profiles supported by installed modules</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8d0b-113">-ModuleName</span><span class="sxs-lookup"><span data-stu-id="e8d0b-113">-ModuleName</span></span>
<span data-ttu-id="e8d0b-114">Имя модуля для проверки.</span><span class="sxs-lookup"><span data-stu-id="e8d0b-114">The name of the module to check</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8d0b-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8d0b-115">CommonParameters</span></span>
<span data-ttu-id="e8d0b-116">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e8d0b-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8d0b-117">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8d0b-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8d0b-118">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e8d0b-118">INPUTS</span></span>

### <span data-ttu-id="e8d0b-119">Ничего</span><span class="sxs-lookup"><span data-stu-id="e8d0b-119">None</span></span>

## <span data-ttu-id="e8d0b-120">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e8d0b-120">OUTPUTS</span></span>

### <span data-ttu-id="e8d0b-121">Microsoft. Azure. Commands. Profile. CommonModule. PSAzureServiceProfile</span><span class="sxs-lookup"><span data-stu-id="e8d0b-121">Microsoft.Azure.Commands.Profile.CommonModule.PSAzureServiceProfile</span></span>

## <span data-ttu-id="e8d0b-122">Пуск</span><span class="sxs-lookup"><span data-stu-id="e8d0b-122">NOTES</span></span>

## <span data-ttu-id="e8d0b-123">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e8d0b-123">RELATED LINKS</span></span>
