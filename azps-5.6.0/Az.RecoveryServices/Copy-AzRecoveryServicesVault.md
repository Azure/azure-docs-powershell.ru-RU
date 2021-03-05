---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/copy-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Copy-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Copy-AzRecoveryServicesVault.md
ms.openlocfilehash: 5b4c7153a844bdc10d2ec487e51ef9f07be0c5c6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101960259"
---
# <span data-ttu-id="dbb13-101">Copy-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="dbb13-101">Copy-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="dbb13-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dbb13-102">SYNOPSIS</span></span>
<span data-ttu-id="dbb13-103">Копирует данные из хранилища в одной области в хранилище в другом регионе.</span><span class="sxs-lookup"><span data-stu-id="dbb13-103">Copies data from a vault in one region to a vault in another region.</span></span>

## <span data-ttu-id="dbb13-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="dbb13-104">SYNTAX</span></span>

```
Copy-AzRecoveryServicesVault [-Force] [-DefaultProfile <IAzureContextContainer>] [-SourceVault] <ARSVault>
 [-TargetVault] <ARSVault> [-RetryOnlyFailed] [<CommonParameters>]
```

## <span data-ttu-id="dbb13-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dbb13-105">DESCRIPTION</span></span>
<span data-ttu-id="dbb13-106">**Cmdlet Copy-AzRecoveryServicesVault** копирует данные из хранилища в одном регионе в хранилище в другом регионе.</span><span class="sxs-lookup"><span data-stu-id="dbb13-106">The **Copy-AzRecoveryServicesVault** cmdlet copies data from a vault in one region to a vault in another region.</span></span> <span data-ttu-id="dbb13-107">В настоящее время поддерживается только перемещение данных на уровне хранилища.</span><span class="sxs-lookup"><span data-stu-id="dbb13-107">Currently we only support vault level data move.</span></span>

## <span data-ttu-id="dbb13-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="dbb13-108">EXAMPLES</span></span>

### <span data-ttu-id="dbb13-109">Пример 1. Копирование данных из хранилища1 в хранилище2</span><span class="sxs-lookup"><span data-stu-id="dbb13-109">Example 1: Copy data from vault1 to vault2</span></span>
```
PS C:\> $sourceVault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName1" -Name "vault1"
PS C:\> $targetVault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName2" -Name "vault2"
PS C:\> Copy-AzRecoveryServicesVault -SourceVault $sourceVault -TargetVault $targetVault
```

<span data-ttu-id="dbb13-110">Первые два cmdlets fetch Recovery Services Vault - vault1 и vault2 соответственно.</span><span class="sxs-lookup"><span data-stu-id="dbb13-110">The first two cmdlets fetch Recovery Services Vault - vault1 and vault2 respectively.</span></span>
<span data-ttu-id="dbb13-111">Вторая команда вызывает полное перемещение данных из хранилища1 в хранилище2.</span><span class="sxs-lookup"><span data-stu-id="dbb13-111">The second command triggers a complete data move from vault1 to vault2.</span></span> 

### <span data-ttu-id="dbb13-112">Пример 2. Копирование данных из хранилища1 в хранилище2 с единственными сбойными элементами</span><span class="sxs-lookup"><span data-stu-id="dbb13-112">Example 2: Copy data from vault1 to vault2 with only failed items</span></span>
```
PS C:\> $sourceVault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName1" -Name "vault1"
PS C:\> $targetVault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName2" -Name "vault2"
PS C:\> Copy-AzRecoveryServicesVault -SourceVault $sourceVault -TargetVault $targetVault -RetryOnlyFailed
```

<span data-ttu-id="dbb13-113">Первые два cmdlets fetch Recovery Services Vault - vault1 и vault2 соответственно.</span><span class="sxs-lookup"><span data-stu-id="dbb13-113">The first two cmdlets fetch Recovery Services Vault - vault1 and vault2 respectively.</span></span>
<span data-ttu-id="dbb13-114">Вторая команда вызывает частичное перемещение данных из хранилища1 в хранилище2 только с теми элементами, которые не удалось в предыдущих операциях перемещения.</span><span class="sxs-lookup"><span data-stu-id="dbb13-114">The second command triggers a partial data move from vault1 to vault2 with only those items which failed in previous move operations.</span></span>

## <span data-ttu-id="dbb13-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dbb13-115">PARAMETERS</span></span>

### <span data-ttu-id="dbb13-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbb13-116">-DefaultProfile</span></span>
<span data-ttu-id="dbb13-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dbb13-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dbb13-118">-Force</span><span class="sxs-lookup"><span data-stu-id="dbb13-118">-Force</span></span>
<span data-ttu-id="dbb13-119">— перемещение данных (диалоговое окно с запросом подтверждения) без запроса подтверждения избыточности для целевого хранилища.</span><span class="sxs-lookup"><span data-stu-id="dbb13-119">Forces the data move operation (prevents confirmation dialog) without asking confirmation for target vault storage redundancy type.</span></span> <span data-ttu-id="dbb13-120">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="dbb13-120">This parameter is optional.</span></span> 

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

### <span data-ttu-id="dbb13-121">-RetryOnlyFailed</span><span class="sxs-lookup"><span data-stu-id="dbb13-121">-RetryOnlyFailed</span></span>
<span data-ttu-id="dbb13-122">Переключите параметр, чтобы попробовать перемещение данных только для контейнеров в исходных хранилищах, которые еще не перемещены.</span><span class="sxs-lookup"><span data-stu-id="dbb13-122">Switch parameter to try data move only for containers in the source vault which are not yet moved.</span></span>

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

### <span data-ttu-id="dbb13-123">-SourceVault</span><span class="sxs-lookup"><span data-stu-id="dbb13-123">-SourceVault</span></span>
<span data-ttu-id="dbb13-124">Исходный объект сейфа, который нужно переместить.</span><span class="sxs-lookup"><span data-stu-id="dbb13-124">The source vault object to be moved.</span></span>

```yaml
Type: ARSVault
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dbb13-125">-TargetVault</span><span class="sxs-lookup"><span data-stu-id="dbb13-125">-TargetVault</span></span>
<span data-ttu-id="dbb13-126">Объект целевого сейфа, данные в который необходимо переместить.</span><span class="sxs-lookup"><span data-stu-id="dbb13-126">The target vault object where the data has to be moved.</span></span>

```yaml
Type: ARSVault
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dbb13-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbb13-127">CommonParameters</span></span>
<span data-ttu-id="dbb13-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dbb13-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbb13-129">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dbb13-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbb13-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dbb13-130">INPUTS</span></span>

### <span data-ttu-id="dbb13-131">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span><span class="sxs-lookup"><span data-stu-id="dbb13-131">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="dbb13-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="dbb13-132">OUTPUTS</span></span>

### <span data-ttu-id="dbb13-133">System.String</span><span class="sxs-lookup"><span data-stu-id="dbb13-133">System.String</span></span>

## <span data-ttu-id="dbb13-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="dbb13-134">NOTES</span></span>

## <span data-ttu-id="dbb13-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dbb13-135">RELATED LINKS</span></span>
