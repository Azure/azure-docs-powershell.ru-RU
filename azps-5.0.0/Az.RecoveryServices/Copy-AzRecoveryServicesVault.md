---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/copy-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Copy-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Copy-AzRecoveryServicesVault.md
ms.openlocfilehash: 630dc1a3a14beec147dec3f7bd2601ed0666ad78
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248221"
---
# <span data-ttu-id="55601-101">Copy-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="55601-101">Copy-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="55601-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="55601-102">SYNOPSIS</span></span>
<span data-ttu-id="55601-103">Копирует данные из хранилища в одном регионе в хранилище другого региона.</span><span class="sxs-lookup"><span data-stu-id="55601-103">Copies data from a vault in one region to a vault in another region.</span></span>

## <span data-ttu-id="55601-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="55601-104">SYNTAX</span></span>

```
Copy-AzRecoveryServicesVault [-Force] [-DefaultProfile <IAzureContextContainer>] [-SourceVault] <ARSVault>
 [-TargetVault] <ARSVault> [-RetryOnlyFailed] [<CommonParameters>]
```

## <span data-ttu-id="55601-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="55601-105">DESCRIPTION</span></span>
<span data-ttu-id="55601-106">Командлет **Copy-AzRecoveryServicesVault** копирует данные из хранилища в одном регионе в хранилище другого региона.</span><span class="sxs-lookup"><span data-stu-id="55601-106">The **Copy-AzRecoveryServicesVault** cmdlet copies data from a vault in one region to a vault in another region.</span></span> <span data-ttu-id="55601-107">В настоящее время только перемещение данных уровня хранилища поддерживается.</span><span class="sxs-lookup"><span data-stu-id="55601-107">Currently we only support vault level data move.</span></span>

## <span data-ttu-id="55601-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="55601-108">EXAMPLES</span></span>

### <span data-ttu-id="55601-109">Пример 1: копирование данных из vault1 в vault2</span><span class="sxs-lookup"><span data-stu-id="55601-109">Example 1: Copy data from vault1 to vault2</span></span>
```powershell
PS C:\> $sourceVault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName1" -Name "vault1"
PS C:\> $targetVault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName2" -Name "vault2"
PS C:\> Copy-AzRecoveryServicesVault -SourceVault $sourceVault -TargetVault $targetVault
```git 

The first two cmdlets fetch Recovery Services Vault - vault1 and vault2 respectively.
The second command triggers a complete data move from vault1 to vault2. 

### Example 2: Copy data from vault1 to vault2 with only failed items
```powershell
PS C:\> $sourceVault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName1" -Name "vault1"
PS C:\> $targetVault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName2" -Name "vault2"
PS C:\> Copy-AzRecoveryServicesVault -SourceVault $sourceVault -TargetVault $targetVault -RetryOnlyFailed
```git 

The first two cmdlets fetch Recovery Services Vault - vault1 and vault2 respectively.
The second command triggers a partial data move from vault1 to vault2 with only those items which failed in previous move operations.

## PARAMETERS

### -DefaultProfile
The credentials, account, tenant, and subscription used for communication with Azure.

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

### <span data-ttu-id="55601-110">-Force</span><span class="sxs-lookup"><span data-stu-id="55601-110">-Force</span></span>
<span data-ttu-id="55601-111">Принудительно выполняет операцию перемещения данных (диалоговое окно подтверждения не запрашивает подтверждение) без подтверждения типа избыточности хранилища целевого хранилища.</span><span class="sxs-lookup"><span data-stu-id="55601-111">Forces the data move operation (prevents confirmation dialog) without asking confirmation for target vault storage redundancy type.</span></span> <span data-ttu-id="55601-112">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="55601-112">This parameter is optional.</span></span> 

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

### <span data-ttu-id="55601-113">-RetryOnlyFailed</span><span class="sxs-lookup"><span data-stu-id="55601-113">-RetryOnlyFailed</span></span>
<span data-ttu-id="55601-114">Параметр Switch, чтобы попытаться переместить данные только для контейнеров в исходном хранилище, которые еще не перемещены.</span><span class="sxs-lookup"><span data-stu-id="55601-114">Switch parameter to try data move only for containers in the source vault which are not yet moved.</span></span>

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

### <span data-ttu-id="55601-115">-SourceVault</span><span class="sxs-lookup"><span data-stu-id="55601-115">-SourceVault</span></span>
<span data-ttu-id="55601-116">Объект исходного хранилища, который нужно переместить.</span><span class="sxs-lookup"><span data-stu-id="55601-116">The source vault object to be moved.</span></span>

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

### <span data-ttu-id="55601-117">-TargetVault</span><span class="sxs-lookup"><span data-stu-id="55601-117">-TargetVault</span></span>
<span data-ttu-id="55601-118">Объект целевого хранилища, куда нужно переместить данные.</span><span class="sxs-lookup"><span data-stu-id="55601-118">The target vault object where the data has to be moved.</span></span>

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

### <span data-ttu-id="55601-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55601-119">CommonParameters</span></span>
<span data-ttu-id="55601-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="55601-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55601-121">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="55601-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55601-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="55601-122">INPUTS</span></span>

### <span data-ttu-id="55601-123">Microsoft. Azure. Commands. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="55601-123">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="55601-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="55601-124">OUTPUTS</span></span>

### <span data-ttu-id="55601-125">System. String</span><span class="sxs-lookup"><span data-stu-id="55601-125">System.String</span></span>

## <span data-ttu-id="55601-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="55601-126">NOTES</span></span>

## <span data-ttu-id="55601-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="55601-127">RELATED LINKS</span></span>
