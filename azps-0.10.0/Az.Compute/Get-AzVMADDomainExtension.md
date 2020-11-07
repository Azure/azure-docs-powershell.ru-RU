---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 49D17667-35C3-4A79-A0C8-C197DAA5CD90
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmaddomainextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMADDomainExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMADDomainExtension.md
ms.openlocfilehash: 809246520c4e6b07a1aca406ef3ec17eb9df31f1
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911543"
---
# <span data-ttu-id="a9c0a-101">Get-AzVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="a9c0a-101">Get-AzVMADDomainExtension</span></span>

## <span data-ttu-id="a9c0a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a9c0a-102">SYNOPSIS</span></span>
<span data-ttu-id="a9c0a-103">Получает сведения о расширении доменных имен Active Directory.</span><span class="sxs-lookup"><span data-stu-id="a9c0a-103">Gets information about an AD domain extension.</span></span>

## <span data-ttu-id="a9c0a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a9c0a-104">SYNTAX</span></span>

```
Get-AzVMADDomainExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a9c0a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a9c0a-105">DESCRIPTION</span></span>
<span data-ttu-id="a9c0a-106">Командлет **Get-AzVMADDomainExtension** получает сведения об указанном расширении домена Azure Active Directory (AD).</span><span class="sxs-lookup"><span data-stu-id="a9c0a-106">The **Get-AzVMADDomainExtension** cmdlet gets information about the specified Azure Active Directory (AD) domain extension.</span></span>

## <span data-ttu-id="a9c0a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a9c0a-107">EXAMPLES</span></span>

### <span data-ttu-id="a9c0a-108">1:</span><span class="sxs-lookup"><span data-stu-id="a9c0a-108">1:</span></span>
```

```

## <span data-ttu-id="a9c0a-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a9c0a-109">PARAMETERS</span></span>

### <span data-ttu-id="a9c0a-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9c0a-110">-DefaultProfile</span></span>
<span data-ttu-id="a9c0a-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a9c0a-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a9c0a-112">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a9c0a-112">-Name</span></span>
<span data-ttu-id="a9c0a-113">Указывает имя расширения домена.</span><span class="sxs-lookup"><span data-stu-id="a9c0a-113">Specifies the name of the domain extension.</span></span>

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

### <span data-ttu-id="a9c0a-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9c0a-114">-ResourceGroupName</span></span>
<span data-ttu-id="a9c0a-115">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a9c0a-115">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="a9c0a-116">-Status (состояние)</span><span class="sxs-lookup"><span data-stu-id="a9c0a-116">-Status</span></span>
<span data-ttu-id="a9c0a-117">Указывает на то, что этот командлет получает представление экземпляра расширения домена.</span><span class="sxs-lookup"><span data-stu-id="a9c0a-117">Indicates that this cmdlet gets the instance view of the domain extension.</span></span>

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

### <span data-ttu-id="a9c0a-118">-VMName</span><span class="sxs-lookup"><span data-stu-id="a9c0a-118">-VMName</span></span>
<span data-ttu-id="a9c0a-119">Указывает имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="a9c0a-119">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="a9c0a-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9c0a-120">CommonParameters</span></span>
<span data-ttu-id="a9c0a-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a9c0a-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9c0a-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9c0a-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9c0a-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a9c0a-123">INPUTS</span></span>

### <span data-ttu-id="a9c0a-124">Ничего</span><span class="sxs-lookup"><span data-stu-id="a9c0a-124">None</span></span>
<span data-ttu-id="a9c0a-125">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="a9c0a-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a9c0a-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a9c0a-126">OUTPUTS</span></span>

### <span data-ttu-id="a9c0a-127">Microsoft. Azure. Commands. COMPUTE. Models. VirtualMachineADDomainExtensionContext</span><span class="sxs-lookup"><span data-stu-id="a9c0a-127">Microsoft.Azure.Commands.Compute.Models.VirtualMachineADDomainExtensionContext</span></span>

## <span data-ttu-id="a9c0a-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="a9c0a-128">NOTES</span></span>

## <span data-ttu-id="a9c0a-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a9c0a-129">RELATED LINKS</span></span>

[<span data-ttu-id="a9c0a-130">Set-AzVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="a9c0a-130">Set-AzVMADDomainExtension</span></span>](./Set-AzVMADDomainExtension.md)


