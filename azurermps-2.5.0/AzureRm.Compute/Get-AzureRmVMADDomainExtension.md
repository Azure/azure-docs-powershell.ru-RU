---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 49D17667-35C3-4A79-A0C8-C197DAA5CD90
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmaddomainextension
schema: 2.0.0
ms.openlocfilehash: 01a5a69053cfd05186abae45d5b53fff0b022b98
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913677"
---
# <span data-ttu-id="b47ea-101">Get-AzureRmVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="b47ea-101">Get-AzureRmVMADDomainExtension</span></span>

## <span data-ttu-id="b47ea-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b47ea-102">SYNOPSIS</span></span>
<span data-ttu-id="b47ea-103">Получает сведения о расширении доменных имен Active Directory.</span><span class="sxs-lookup"><span data-stu-id="b47ea-103">Gets information about an AD domain extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b47ea-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b47ea-104">SYNTAX</span></span>

```
Get-AzureRmVMADDomainExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b47ea-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b47ea-105">DESCRIPTION</span></span>
<span data-ttu-id="b47ea-106">Командлет **Get-AzureRmVMADDomainExtension** получает сведения об указанном расширении домена Azure Active Directory (AD).</span><span class="sxs-lookup"><span data-stu-id="b47ea-106">The **Get-AzureRmVMADDomainExtension** cmdlet gets information about the specified Azure Active Directory (AD) domain extension.</span></span>

## <span data-ttu-id="b47ea-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b47ea-107">EXAMPLES</span></span>

### <span data-ttu-id="b47ea-108">1:</span><span class="sxs-lookup"><span data-stu-id="b47ea-108">1:</span></span>
```

```

## <span data-ttu-id="b47ea-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b47ea-109">PARAMETERS</span></span>

### <span data-ttu-id="b47ea-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b47ea-110">-DefaultProfile</span></span>
<span data-ttu-id="b47ea-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b47ea-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b47ea-112">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b47ea-112">-Name</span></span>
<span data-ttu-id="b47ea-113">Указывает имя расширения домена.</span><span class="sxs-lookup"><span data-stu-id="b47ea-113">Specifies the name of the domain extension.</span></span>

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

### <span data-ttu-id="b47ea-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b47ea-114">-ResourceGroupName</span></span>
<span data-ttu-id="b47ea-115">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b47ea-115">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="b47ea-116">-Status (состояние)</span><span class="sxs-lookup"><span data-stu-id="b47ea-116">-Status</span></span>
<span data-ttu-id="b47ea-117">Указывает на то, что этот командлет получает представление экземпляра расширения домена.</span><span class="sxs-lookup"><span data-stu-id="b47ea-117">Indicates that this cmdlet gets the instance view of the domain extension.</span></span>

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

### <span data-ttu-id="b47ea-118">-VMName</span><span class="sxs-lookup"><span data-stu-id="b47ea-118">-VMName</span></span>
<span data-ttu-id="b47ea-119">Указывает имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="b47ea-119">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="b47ea-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b47ea-120">CommonParameters</span></span>
<span data-ttu-id="b47ea-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b47ea-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b47ea-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b47ea-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b47ea-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b47ea-123">INPUTS</span></span>

### <span data-ttu-id="b47ea-124">Ничего</span><span class="sxs-lookup"><span data-stu-id="b47ea-124">None</span></span>
<span data-ttu-id="b47ea-125">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="b47ea-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b47ea-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b47ea-126">OUTPUTS</span></span>

### <span data-ttu-id="b47ea-127">Microsoft. Azure. Commands. COMPUTE. Models. VirtualMachineADDomainExtensionContext</span><span class="sxs-lookup"><span data-stu-id="b47ea-127">Microsoft.Azure.Commands.Compute.Models.VirtualMachineADDomainExtensionContext</span></span>

## <span data-ttu-id="b47ea-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="b47ea-128">NOTES</span></span>

## <span data-ttu-id="b47ea-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b47ea-129">RELATED LINKS</span></span>

[<span data-ttu-id="b47ea-130">Set-AzureRmVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="b47ea-130">Set-AzureRmVMADDomainExtension</span></span>](./Set-AzureRmVMADDomainExtension.md)


