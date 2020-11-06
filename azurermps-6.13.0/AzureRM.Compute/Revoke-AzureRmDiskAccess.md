---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/revoke-azurermdiskaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Revoke-AzureRmDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Revoke-AzureRmDiskAccess.md
ms.openlocfilehash: a0b6ddf2a5796c63c3efd20b811a2040db123836
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568941"
---
# <span data-ttu-id="31869-101">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="31869-101">Revoke-AzureRmDiskAccess</span></span>

## <span data-ttu-id="31869-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="31869-102">SYNOPSIS</span></span>
<span data-ttu-id="31869-103">Отменяет доступ к диску.</span><span class="sxs-lookup"><span data-stu-id="31869-103">Revokes an access to a disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="31869-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="31869-104">SYNTAX</span></span>

```
Revoke-AzureRmDiskAccess [-ResourceGroupName] <String> [-DiskName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="31869-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="31869-105">DESCRIPTION</span></span>
<span data-ttu-id="31869-106">Командлет **REVOKE-AzureRmDiskAccess** отменяет доступ к диску.</span><span class="sxs-lookup"><span data-stu-id="31869-106">The **Revoke-AzureRmDiskAccess** cmdlet revokes an access to a disk.</span></span>

## <span data-ttu-id="31869-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="31869-107">EXAMPLES</span></span>

### <span data-ttu-id="31869-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="31869-108">Example 1</span></span>
```
PS C:\> Revoke-AzureRmDiskAccess -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'
```

<span data-ttu-id="31869-109">Отмена доступа к диску с именем "Disk01" в группе ресурсов с именем "ResourceGroup01"</span><span class="sxs-lookup"><span data-stu-id="31869-109">Revoke the access to the disk named 'Disk01' in the resource group named 'ResourceGroup01'</span></span>

## <span data-ttu-id="31869-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="31869-110">PARAMETERS</span></span>

### <span data-ttu-id="31869-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="31869-111">-AsJob</span></span>
<span data-ttu-id="31869-112">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="31869-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="31869-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31869-113">-DefaultProfile</span></span>
<span data-ttu-id="31869-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="31869-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="31869-115">-DiskName</span><span class="sxs-lookup"><span data-stu-id="31869-115">-DiskName</span></span>
<span data-ttu-id="31869-116">Указывает имя диска.</span><span class="sxs-lookup"><span data-stu-id="31869-116">Specifies the name of a disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31869-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31869-117">-ResourceGroupName</span></span>
<span data-ttu-id="31869-118">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="31869-118">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31869-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="31869-119">-Confirm</span></span>
<span data-ttu-id="31869-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="31869-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="31869-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31869-121">-WhatIf</span></span>
<span data-ttu-id="31869-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="31869-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="31869-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="31869-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="31869-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31869-124">CommonParameters</span></span>
<span data-ttu-id="31869-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="31869-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31869-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31869-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31869-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="31869-127">INPUTS</span></span>

### <span data-ttu-id="31869-128">System. String</span><span class="sxs-lookup"><span data-stu-id="31869-128">System.String</span></span>

## <span data-ttu-id="31869-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="31869-129">OUTPUTS</span></span>

### <span data-ttu-id="31869-130">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="31869-130">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="31869-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="31869-131">NOTES</span></span>

## <span data-ttu-id="31869-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="31869-132">RELATED LINKS</span></span>
