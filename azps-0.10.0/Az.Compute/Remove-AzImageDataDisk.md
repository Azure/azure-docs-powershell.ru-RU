---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azimagedatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzImageDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzImageDataDisk.md
ms.openlocfilehash: 3c7399e3eec760e8d4a40d58a8ea9a56e744cfd4
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911433"
---
# <span data-ttu-id="ec866-101">Remove-AzImageDataDisk</span><span class="sxs-lookup"><span data-stu-id="ec866-101">Remove-AzImageDataDisk</span></span>

## <span data-ttu-id="ec866-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ec866-102">SYNOPSIS</span></span>
<span data-ttu-id="ec866-103">Удаляет диск с данными из объекта Image.</span><span class="sxs-lookup"><span data-stu-id="ec866-103">Removes a data disk from an image object.</span></span>

## <span data-ttu-id="ec866-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ec866-104">SYNTAX</span></span>

```
Remove-AzImageDataDisk [-Image] <PSImage> [-Lun] <Int32> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ec866-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ec866-105">DESCRIPTION</span></span>
<span data-ttu-id="ec866-106">Командлет **Remove-AzImageDataDisk** удаляет диск с данными из объекта Image.</span><span class="sxs-lookup"><span data-stu-id="ec866-106">The **Remove-AzImageDataDisk** cmdlet removes a data disk from an image object.</span></span>

## <span data-ttu-id="ec866-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ec866-107">EXAMPLES</span></span>

### <span data-ttu-id="ec866-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ec866-108">Example 1</span></span>
```
PS C:\> Get-AzImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' | Remove-AzImageDataDisk -Lun 1 | Update-AzImage;
```

<span data-ttu-id="ec866-109">Эта команда удаляет диск данных логического устройства с номером 1 из существующего образа "image01" в группе ресурсов "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="ec866-109">This command removes the data disk of logical unit number 1 from the existing image 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="ec866-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ec866-110">PARAMETERS</span></span>

### <span data-ttu-id="ec866-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec866-111">-DefaultProfile</span></span>
<span data-ttu-id="ec866-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ec866-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ec866-113">-Image</span><span class="sxs-lookup"><span data-stu-id="ec866-113">-Image</span></span>
<span data-ttu-id="ec866-114">Указывает локальный объект изображения.</span><span class="sxs-lookup"><span data-stu-id="ec866-114">Specifies a local image object.</span></span>

```yaml
Type: PSImage
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ec866-115">-LUN</span><span class="sxs-lookup"><span data-stu-id="ec866-115">-Lun</span></span>
<span data-ttu-id="ec866-116">Задает логический номер устройства (LUN).</span><span class="sxs-lookup"><span data-stu-id="ec866-116">Specifies the logical unit number (LUN).</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec866-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ec866-117">-Confirm</span></span>
<span data-ttu-id="ec866-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ec866-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec866-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec866-119">-WhatIf</span></span>
<span data-ttu-id="ec866-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ec866-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ec866-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ec866-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec866-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec866-122">CommonParameters</span></span>
<span data-ttu-id="ec866-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ec866-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec866-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec866-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec866-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ec866-125">INPUTS</span></span>

### <span data-ttu-id="ec866-126">Microsoft. Azure. Management. COMPUTE. Models.</span><span class="sxs-lookup"><span data-stu-id="ec866-126">Microsoft.Azure.Management.Compute.Models.Image</span></span>
<span data-ttu-id="ec866-127">System. Nullable "1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="ec866-127">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="ec866-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ec866-128">OUTPUTS</span></span>

### <span data-ttu-id="ec866-129">Microsoft. Azure. Management. COMPUTE. Models.</span><span class="sxs-lookup"><span data-stu-id="ec866-129">Microsoft.Azure.Management.Compute.Models.Image</span></span>

## <span data-ttu-id="ec866-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="ec866-130">NOTES</span></span>

## <span data-ttu-id="ec866-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ec866-131">RELATED LINKS</span></span>

