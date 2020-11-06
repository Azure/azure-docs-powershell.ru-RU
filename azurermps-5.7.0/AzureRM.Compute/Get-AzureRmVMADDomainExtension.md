---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 49D17667-35C3-4A79-A0C8-C197DAA5CD90
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMADDomainExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMADDomainExtension.md
ms.openlocfilehash: d55d84560ca75a508a05276d8d33eb78d1d50ab5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565567"
---
# <span data-ttu-id="f1766-101">Get-AzureRmVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="f1766-101">Get-AzureRmVMADDomainExtension</span></span>

## <span data-ttu-id="f1766-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f1766-102">SYNOPSIS</span></span>
<span data-ttu-id="f1766-103">Получает сведения о расширении доменных имен Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f1766-103">Gets information about an AD domain extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f1766-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f1766-104">SYNTAX</span></span>

```
Get-AzureRmVMADDomainExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [<CommonParameters>]
```

## <span data-ttu-id="f1766-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f1766-105">DESCRIPTION</span></span>
<span data-ttu-id="f1766-106">Командлет **Get-AzureRmVMADDomainExtension** получает сведения об указанном расширении домена Azure Active Directory (AD).</span><span class="sxs-lookup"><span data-stu-id="f1766-106">The **Get-AzureRmVMADDomainExtension** cmdlet gets information about the specified Azure Active Directory (AD) domain extension.</span></span>

## <span data-ttu-id="f1766-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f1766-107">EXAMPLES</span></span>

## <span data-ttu-id="f1766-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f1766-108">PARAMETERS</span></span>

### <span data-ttu-id="f1766-109">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f1766-109">-Name</span></span>
<span data-ttu-id="f1766-110">Указывает имя расширения домена.</span><span class="sxs-lookup"><span data-stu-id="f1766-110">Specifies the name of the domain extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1766-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1766-111">-ResourceGroupName</span></span>
<span data-ttu-id="f1766-112">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f1766-112">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1766-113">-Status (состояние)</span><span class="sxs-lookup"><span data-stu-id="f1766-113">-Status</span></span>
<span data-ttu-id="f1766-114">Указывает на то, что этот командлет получает представление экземпляра расширения домена.</span><span class="sxs-lookup"><span data-stu-id="f1766-114">Indicates that this cmdlet gets the instance view of the domain extension.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1766-115">-VMName</span><span class="sxs-lookup"><span data-stu-id="f1766-115">-VMName</span></span>
<span data-ttu-id="f1766-116">Указывает имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="f1766-116">Specifies the name of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1766-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1766-117">CommonParameters</span></span>
<span data-ttu-id="f1766-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f1766-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1766-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1766-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1766-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f1766-120">INPUTS</span></span>

### <span data-ttu-id="f1766-121">Ничего</span><span class="sxs-lookup"><span data-stu-id="f1766-121">None</span></span>
<span data-ttu-id="f1766-122">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="f1766-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f1766-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f1766-123">OUTPUTS</span></span>

## <span data-ttu-id="f1766-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="f1766-124">NOTES</span></span>

## <span data-ttu-id="f1766-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f1766-125">RELATED LINKS</span></span>

[<span data-ttu-id="f1766-126">Set-AzureRmVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="f1766-126">Set-AzureRmVMADDomainExtension</span></span>](./Set-AzureRmVMADDomainExtension.md)


