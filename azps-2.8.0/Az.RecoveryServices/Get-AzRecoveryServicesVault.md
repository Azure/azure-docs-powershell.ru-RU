---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 818B5302-91EE-425F-B1CD-86B626F1B7A3
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVault.md
ms.openlocfilehash: 3607835496aa6f99cfd2b42383654180d6b12331
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93904878"
---
# <span data-ttu-id="a7f0c-101">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="a7f0c-101">Get-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="a7f0c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a7f0c-102">SYNOPSIS</span></span>

<span data-ttu-id="a7f0c-103">Получает список хранилищ служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="a7f0c-103">Gets a list of Recovery Services vaults.</span></span>

## <span data-ttu-id="a7f0c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a7f0c-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesVault [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a7f0c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a7f0c-105">DESCRIPTION</span></span>

<span data-ttu-id="a7f0c-106">Командлет **Get-AzRecoveryServicesVault** получает список хранилищ служб восстановления в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="a7f0c-106">The **Get-AzRecoveryServicesVault** cmdlet gets a list of Recovery Services vaults in the current subscription.</span></span>

## <span data-ttu-id="a7f0c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a7f0c-107">EXAMPLES</span></span>

### <span data-ttu-id="a7f0c-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a7f0c-108">Example 1</span></span>

```powershell
PS C:\> Get-AzRecoveryServicesVault
```

<span data-ttu-id="a7f0c-109">Получение списка хранилищ в выбранной подписке.</span><span class="sxs-lookup"><span data-stu-id="a7f0c-109">Get the list of vault in selected subscription.</span></span>

### <span data-ttu-id="a7f0c-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="a7f0c-110">Example 2</span></span>

```powershell
PS C:\> Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup"
```

<span data-ttu-id="a7f0c-111">Получение списка хранилищ в группе ресурсов в выбранной подписке.</span><span class="sxs-lookup"><span data-stu-id="a7f0c-111">Get the list of vault in resource group in selected subscription.</span></span>

### <span data-ttu-id="a7f0c-112">Пример 3</span><span class="sxs-lookup"><span data-stu-id="a7f0c-112">Example 3</span></span>

```powershell
PS C:\> Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
```

<span data-ttu-id="a7f0c-113">Получение хранилища в группе ресурсов с указанным именем.</span><span class="sxs-lookup"><span data-stu-id="a7f0c-113">Get the vault in resource group with given name.</span></span>

## <span data-ttu-id="a7f0c-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a7f0c-114">PARAMETERS</span></span>

### <span data-ttu-id="a7f0c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7f0c-115">-DefaultProfile</span></span>

<span data-ttu-id="a7f0c-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a7f0c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7f0c-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a7f0c-117">-Name</span></span>

<span data-ttu-id="a7f0c-118">Указывает имя хранилища для запроса.</span><span class="sxs-lookup"><span data-stu-id="a7f0c-118">Specifies the name of the vault to query for.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7f0c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7f0c-119">-ResourceGroupName</span></span>

<span data-ttu-id="a7f0c-120">Указывает имя группы ресурсов Azure, из которой извлекается указанный объект служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="a7f0c-120">Specifies the name of the Azure resource group from which to retrieve the specified Recovery Services object.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7f0c-121">-CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7f0c-121">-CommonParameters</span></span>

<span data-ttu-id="a7f0c-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a7f0c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7f0c-123">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a7f0c-123">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7f0c-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a7f0c-124">INPUTS</span></span>

### <span data-ttu-id="a7f0c-125">Ничего</span><span class="sxs-lookup"><span data-stu-id="a7f0c-125">None</span></span>

## <span data-ttu-id="a7f0c-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a7f0c-126">OUTPUTS</span></span>

### <span data-ttu-id="a7f0c-127">Microsoft. Azure. Commands. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="a7f0c-127">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="a7f0c-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="a7f0c-128">NOTES</span></span>

## <span data-ttu-id="a7f0c-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a7f0c-129">RELATED LINKS</span></span>

[<span data-ttu-id="a7f0c-130">Get-AzRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="a7f0c-130">Get-AzRecoveryServicesVaultSettingsFile</span></span>](./Get-AzRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="a7f0c-131">New-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="a7f0c-131">New-AzRecoveryServicesVault</span></span>](./New-AzRecoveryServicesVault.md)

[<span data-ttu-id="a7f0c-132">Remove-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="a7f0c-132">Remove-AzRecoveryServicesVault</span></span>](./Remove-AzRecoveryServicesVault.md)
