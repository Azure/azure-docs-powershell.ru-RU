---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilespool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesPool.md
ms.openlocfilehash: 717c1cac6def6fb51f1ab8b598f15a05a7d62db4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93911743"
---
# <span data-ttu-id="12bb3-101">Remove-AzNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="12bb3-101">Remove-AzNetAppFilesPool</span></span>

## <span data-ttu-id="12bb3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="12bb3-102">SYNOPSIS</span></span>
<span data-ttu-id="12bb3-103">Удаление пула файлов Azure NetApp (ANF).</span><span class="sxs-lookup"><span data-stu-id="12bb3-103">Deletes an Azure NetApp Files (ANF) pool.</span></span>

## <span data-ttu-id="12bb3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="12bb3-104">SYNTAX</span></span>

### <span data-ttu-id="12bb3-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="12bb3-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesPool -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12bb3-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="12bb3-106">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesPool -Name <String> -AccountObject <PSNetAppFilesAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12bb3-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="12bb3-107">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesPool -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12bb3-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="12bb3-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesPool -InputObject <PSNetAppFilesPool> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="12bb3-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="12bb3-109">DESCRIPTION</span></span>
<span data-ttu-id="12bb3-110">Командлет **Remove-AzNetAppFilesPool** УДАЛЯЕТ пул ANF.</span><span class="sxs-lookup"><span data-stu-id="12bb3-110">The **Remove-AzNetAppFilesPool** cmdlet deletes an ANF pool.</span></span>

## <span data-ttu-id="12bb3-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="12bb3-111">EXAMPLES</span></span>

### <span data-ttu-id="12bb3-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="12bb3-112">Example 1</span></span>
```
PS C:\>Remove-AzNetAppFilesPool -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool"
```

<span data-ttu-id="12bb3-113">Эта команда удаляет пул ANF "MyAnfPool".</span><span class="sxs-lookup"><span data-stu-id="12bb3-113">This command deletes the ANF pool "MyAnfPool".</span></span>

## <span data-ttu-id="12bb3-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="12bb3-114">PARAMETERS</span></span>

### <span data-ttu-id="12bb3-115">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="12bb3-115">-AccountName</span></span>
<span data-ttu-id="12bb3-116">Имя учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="12bb3-116">The name of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12bb3-117">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="12bb3-117">-AccountObject</span></span>
<span data-ttu-id="12bb3-118">Объект Account, содержащий пул, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="12bb3-118">The account object containing the pool to remove</span></span>

```yaml
Type: PSNetAppFilesAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="12bb3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12bb3-119">-DefaultProfile</span></span>
<span data-ttu-id="12bb3-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="12bb3-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12bb3-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="12bb3-121">-InputObject</span></span>
<span data-ttu-id="12bb3-122">Объект пула, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="12bb3-122">The pool object to remove</span></span>

```yaml
Type: PSNetAppFilesPool
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="12bb3-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="12bb3-123">-Name</span></span>
<span data-ttu-id="12bb3-124">Название пула ANF</span><span class="sxs-lookup"><span data-stu-id="12bb3-124">The name of the ANF pool</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: PoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12bb3-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="12bb3-125">-PassThru</span></span>
<span data-ttu-id="12bb3-126">Возвращает значение, указывающее, был ли указанный пул успешно удален</span><span class="sxs-lookup"><span data-stu-id="12bb3-126">Return whether the specified pool was successfully removed</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12bb3-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12bb3-127">-ResourceGroupName</span></span>
<span data-ttu-id="12bb3-128">Группа ресурсов в пуле ANF</span><span class="sxs-lookup"><span data-stu-id="12bb3-128">The resource group of the ANF pool</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12bb3-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="12bb3-129">-ResourceId</span></span>
<span data-ttu-id="12bb3-130">Идентификатор ресурса пула ANF</span><span class="sxs-lookup"><span data-stu-id="12bb3-130">The resource id of the ANF pool</span></span>

```yaml
Type: String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12bb3-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="12bb3-131">-Confirm</span></span>
<span data-ttu-id="12bb3-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="12bb3-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12bb3-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12bb3-133">-WhatIf</span></span>
<span data-ttu-id="12bb3-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="12bb3-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12bb3-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="12bb3-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12bb3-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12bb3-136">CommonParameters</span></span>
<span data-ttu-id="12bb3-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="12bb3-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="12bb3-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12bb3-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12bb3-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="12bb3-139">INPUTS</span></span>

### <span data-ttu-id="12bb3-140">System. String</span><span class="sxs-lookup"><span data-stu-id="12bb3-140">System.String</span></span>

### <span data-ttu-id="12bb3-141">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="12bb3-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="12bb3-142">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="12bb3-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="12bb3-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="12bb3-143">OUTPUTS</span></span>

### <span data-ttu-id="12bb3-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="12bb3-144">System.Boolean</span></span>

## <span data-ttu-id="12bb3-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="12bb3-145">NOTES</span></span>

## <span data-ttu-id="12bb3-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="12bb3-146">RELATED LINKS</span></span>
