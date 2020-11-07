---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilespool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesPool.md
ms.openlocfilehash: ef896185b606e107bb62208255a255655814fcbc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93902613"
---
# <span data-ttu-id="514cf-101">Remove-AzNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="514cf-101">Remove-AzNetAppFilesPool</span></span>

## <span data-ttu-id="514cf-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="514cf-102">SYNOPSIS</span></span>
<span data-ttu-id="514cf-103">Удаление пула файлов Azure NetApp (ANF).</span><span class="sxs-lookup"><span data-stu-id="514cf-103">Deletes an Azure NetApp Files (ANF) pool.</span></span>

## <span data-ttu-id="514cf-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="514cf-104">SYNTAX</span></span>

### <span data-ttu-id="514cf-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="514cf-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesPool -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="514cf-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="514cf-106">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesPool -Name <String> -AccountObject <PSNetAppFilesAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="514cf-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="514cf-107">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesPool -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="514cf-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="514cf-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesPool -InputObject <PSNetAppFilesPool> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="514cf-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="514cf-109">DESCRIPTION</span></span>
<span data-ttu-id="514cf-110">Командлет **Remove-AzNetAppFilesPool** УДАЛЯЕТ пул ANF.</span><span class="sxs-lookup"><span data-stu-id="514cf-110">The **Remove-AzNetAppFilesPool** cmdlet deletes an ANF pool.</span></span>

## <span data-ttu-id="514cf-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="514cf-111">EXAMPLES</span></span>

### <span data-ttu-id="514cf-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="514cf-112">Example 1</span></span>
```
PS C:\>Remove-AzNetAppFilesPool -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool"
```

<span data-ttu-id="514cf-113">Эта команда удаляет пул ANF "MyAnfPool".</span><span class="sxs-lookup"><span data-stu-id="514cf-113">This command deletes the ANF pool "MyAnfPool".</span></span>

## <span data-ttu-id="514cf-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="514cf-114">PARAMETERS</span></span>

### <span data-ttu-id="514cf-115">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="514cf-115">-AccountName</span></span>
<span data-ttu-id="514cf-116">Имя учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="514cf-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="514cf-117">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="514cf-117">-AccountObject</span></span>
<span data-ttu-id="514cf-118">Объект Account, содержащий пул, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="514cf-118">The account object containing the pool to remove</span></span>

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

### <span data-ttu-id="514cf-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="514cf-119">-DefaultProfile</span></span>
<span data-ttu-id="514cf-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="514cf-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="514cf-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="514cf-121">-InputObject</span></span>
<span data-ttu-id="514cf-122">Объект пула, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="514cf-122">The pool object to remove</span></span>

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

### <span data-ttu-id="514cf-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="514cf-123">-Name</span></span>
<span data-ttu-id="514cf-124">Название пула ANF</span><span class="sxs-lookup"><span data-stu-id="514cf-124">The name of the ANF pool</span></span>

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

### <span data-ttu-id="514cf-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="514cf-125">-PassThru</span></span>
<span data-ttu-id="514cf-126">Возвращает значение, указывающее, был ли указанный пул успешно удален</span><span class="sxs-lookup"><span data-stu-id="514cf-126">Return whether the specified pool was successfully removed</span></span>

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

### <span data-ttu-id="514cf-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="514cf-127">-ResourceGroupName</span></span>
<span data-ttu-id="514cf-128">Группа ресурсов в пуле ANF</span><span class="sxs-lookup"><span data-stu-id="514cf-128">The resource group of the ANF pool</span></span>

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

### <span data-ttu-id="514cf-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="514cf-129">-ResourceId</span></span>
<span data-ttu-id="514cf-130">Идентификатор ресурса пула ANF</span><span class="sxs-lookup"><span data-stu-id="514cf-130">The resource id of the ANF pool</span></span>

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

### <span data-ttu-id="514cf-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="514cf-131">-Confirm</span></span>
<span data-ttu-id="514cf-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="514cf-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="514cf-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="514cf-133">-WhatIf</span></span>
<span data-ttu-id="514cf-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="514cf-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="514cf-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="514cf-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="514cf-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="514cf-136">CommonParameters</span></span>
<span data-ttu-id="514cf-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="514cf-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="514cf-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="514cf-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="514cf-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="514cf-139">INPUTS</span></span>

### <span data-ttu-id="514cf-140">System. String</span><span class="sxs-lookup"><span data-stu-id="514cf-140">System.String</span></span>

### <span data-ttu-id="514cf-141">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="514cf-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="514cf-142">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="514cf-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="514cf-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="514cf-143">OUTPUTS</span></span>

### <span data-ttu-id="514cf-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="514cf-144">System.Boolean</span></span>

## <span data-ttu-id="514cf-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="514cf-145">NOTES</span></span>

## <span data-ttu-id="514cf-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="514cf-146">RELATED LINKS</span></span>
