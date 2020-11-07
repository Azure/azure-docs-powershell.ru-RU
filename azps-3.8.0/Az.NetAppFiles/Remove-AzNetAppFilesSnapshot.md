---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilessnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesSnapshot.md
ms.openlocfilehash: 098f38f259db3eeb79b40dc799845877f5cafb60
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93911744"
---
# <span data-ttu-id="f643c-101">Remove-AzNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="f643c-101">Remove-AzNetAppFilesSnapshot</span></span>

## <span data-ttu-id="f643c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f643c-102">SYNOPSIS</span></span>
<span data-ttu-id="f643c-103">Удаляет снимок NetApp файлов Azure (ANF).</span><span class="sxs-lookup"><span data-stu-id="f643c-103">Deletes an Azure NetApp Files (ANF) snapshot.</span></span>

## <span data-ttu-id="f643c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f643c-104">SYNTAX</span></span>

### <span data-ttu-id="f643c-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f643c-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesSnapshot -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -VolumeName <String> -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f643c-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f643c-106">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesSnapshot -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f643c-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f643c-107">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesSnapshot -VolumeObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f643c-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f643c-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesSnapshot -InputObject <PSNetAppFilesSnapshot> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f643c-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f643c-109">DESCRIPTION</span></span>
<span data-ttu-id="f643c-110">Командлет **Remove-AzNetAppFilesSnapshot** удаляет моментальный снимок ANF.</span><span class="sxs-lookup"><span data-stu-id="f643c-110">The **Remove-AzNetAppFilesSnapshot** cmdlet deletes an ANF snapshot.</span></span>

## <span data-ttu-id="f643c-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f643c-111">EXAMPLES</span></span>

### <span data-ttu-id="f643c-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f643c-112">Example 1</span></span>
```
PS C:\>Remove-AzNetAppFilesSnapshot -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyAnfVolume" -Name "MyAnfSnapshot"
```

<span data-ttu-id="f643c-113">Эта команда удаляет снимок ANF "MyAnfSnapshot".</span><span class="sxs-lookup"><span data-stu-id="f643c-113">This command deletes the ANF snapshot "MyAnfSnapshot".</span></span>

## <span data-ttu-id="f643c-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f643c-114">PARAMETERS</span></span>

### <span data-ttu-id="f643c-115">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="f643c-115">-AccountName</span></span>
<span data-ttu-id="f643c-116">Имя учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="f643c-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="f643c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f643c-117">-DefaultProfile</span></span>
<span data-ttu-id="f643c-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f643c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f643c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f643c-119">-InputObject</span></span>
<span data-ttu-id="f643c-120">Удаляемый объект снимка</span><span class="sxs-lookup"><span data-stu-id="f643c-120">The snapshot object to remove</span></span>

```yaml
Type: PSNetAppFilesSnapshot
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f643c-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f643c-121">-Name</span></span>
<span data-ttu-id="f643c-122">Имя моментального снимка ANF</span><span class="sxs-lookup"><span data-stu-id="f643c-122">The name of the ANF snapshot</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: SnapshotName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f643c-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f643c-123">-PassThru</span></span>
<span data-ttu-id="f643c-124">Возвращает значение, указывающее, был ли успешно удален указанный том</span><span class="sxs-lookup"><span data-stu-id="f643c-124">Return whether the specified volume was successfully removed</span></span>

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

### <span data-ttu-id="f643c-125">-PoolName</span><span class="sxs-lookup"><span data-stu-id="f643c-125">-PoolName</span></span>
<span data-ttu-id="f643c-126">Название пула ANF</span><span class="sxs-lookup"><span data-stu-id="f643c-126">The name of the ANF pool</span></span>

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

### <span data-ttu-id="f643c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f643c-127">-ResourceGroupName</span></span>
<span data-ttu-id="f643c-128">Группа "ресурсы" для моментального снимка ANF</span><span class="sxs-lookup"><span data-stu-id="f643c-128">The resource group of the ANF snapshot</span></span>

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

### <span data-ttu-id="f643c-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f643c-129">-ResourceId</span></span>
<span data-ttu-id="f643c-130">Идентификатор ресурса для моментального снимка ANF</span><span class="sxs-lookup"><span data-stu-id="f643c-130">The resource id of the ANF snapshot</span></span>

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

### <span data-ttu-id="f643c-131">-Тома</span><span class="sxs-lookup"><span data-stu-id="f643c-131">-VolumeName</span></span>
<span data-ttu-id="f643c-132">Имя ANFого тома.</span><span class="sxs-lookup"><span data-stu-id="f643c-132">The name of the ANF volume</span></span>

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

### <span data-ttu-id="f643c-133">-VolumeObject</span><span class="sxs-lookup"><span data-stu-id="f643c-133">-VolumeObject</span></span>
<span data-ttu-id="f643c-134">Объект Volume, содержащий удаляемый снимок.</span><span class="sxs-lookup"><span data-stu-id="f643c-134">The volume object containing the snapshot to remove</span></span>

```yaml
Type: PSNetAppFilesVolume
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f643c-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f643c-135">-Confirm</span></span>
<span data-ttu-id="f643c-136">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f643c-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f643c-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f643c-137">-WhatIf</span></span>
<span data-ttu-id="f643c-138">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f643c-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f643c-139">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f643c-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f643c-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f643c-140">CommonParameters</span></span>
<span data-ttu-id="f643c-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f643c-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="f643c-142">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f643c-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f643c-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f643c-143">INPUTS</span></span>

### <span data-ttu-id="f643c-144">System. String</span><span class="sxs-lookup"><span data-stu-id="f643c-144">System.String</span></span>

### <span data-ttu-id="f643c-145">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="f643c-145">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

### <span data-ttu-id="f643c-146">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="f643c-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshot</span></span>

## <span data-ttu-id="f643c-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f643c-147">OUTPUTS</span></span>

### <span data-ttu-id="f643c-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f643c-148">System.Boolean</span></span>

## <span data-ttu-id="f643c-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="f643c-149">NOTES</span></span>

## <span data-ttu-id="f643c-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f643c-150">RELATED LINKS</span></span>
